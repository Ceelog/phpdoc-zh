ncurses\_addch
==============

Add character at current position and advance cursor

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_addch</span> ( <span
class="methodparam"><span class="type">int</span> `$ch`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ch`  

ncurses\_addchnstr
==================

Add attributed string with specified length at current position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_addchnstr</span> ( <span
class="methodparam"><span class="type">string</span> `$s`</span> , <span
class="methodparam"><span class="type">int</span> `$n`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`s`  

`n`  

ncurses\_addchstr
=================

Add attributed string at current position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_addchstr</span> ( <span
class="methodparam"><span class="type">string</span> `$s`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`s`  

ncurses\_addnstr
================

Add string with specified length at current position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_addnstr</span> ( <span
class="methodparam"><span class="type">string</span> `$s`</span> , <span
class="methodparam"><span class="type">int</span> `$n`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`s`  

`n`  

ncurses\_addstr
===============

Output text at current position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_addstr</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`text`  

ncurses\_assume\_default\_colors
================================

Define default colors for color 0

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_assume\_default\_colors</span> ( <span
class="methodparam"><span class="type">int</span> `$fg`</span> , <span
class="methodparam"><span class="type">int</span> `$bg`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`fg`  

`bg`  

ncurses\_attroff
================

Turn off the given attributes

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_attroff</span> ( <span
class="methodparam"><span class="type">int</span> `$attributes`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`attributes`  

ncurses\_attron
===============

Turn on the given attributes

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_attron</span> ( <span
class="methodparam"><span class="type">int</span> `$attributes`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`attributes`  

ncurses\_attrset
================

Set given attributes

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_attrset</span> ( <span
class="methodparam"><span class="type">int</span> `$attributes`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`attributes`  

ncurses\_baudrate
=================

Returns baudrate of terminal

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_baudrate</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_beep
=============

Let the terminal beep

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_beep</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">ncurses\_beep</span> sends an audible alert
(bell) and if its not possible flashes the screen.

### 参见

-   <span class="function">ncurses\_flash</span>

ncurses\_bkgd
=============

Set background property for terminal screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_bkgd</span> ( <span
class="methodparam"><span class="type">int</span> `$attrchar`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`attrchar`  

ncurses\_bkgdset
================

Control screen background

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_bkgdset</span> ( <span
class="methodparam"><span class="type">int</span> `$attrchar`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`attrchar`  

ncurses\_border
===============

Draw a border around the screen using attributed characters

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_border</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$right`</span> ,
<span class="methodparam"><span class="type">int</span> `$top`</span> ,
<span class="methodparam"><span class="type">int</span> `$bottom`</span>
, <span class="methodparam"><span class="type">int</span>
`$tl_corner`</span> , <span class="methodparam"><span
class="type">int</span> `$tr_corner`</span> , <span
class="methodparam"><span class="type">int</span> `$bl_corner`</span> ,
<span class="methodparam"><span class="type">int</span>
`$br_corner`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Draws the specified lines and corners around the main window.

Use <span class="function">ncurses\_wborder</span> for borders around
subwindows!

### 参数

Every parameter expects 0 to draw a line or 1 to skip it.

`left`  

`right`  

`top`  

`bottom`  

`tl_corner`  
Top left corner

`tr_corner`  
Top right corner

`bl_corner`  
Bottom left corner

`br_corner`  
Bottom right corner

### 参见

-   <span class="function">ncurses\_wborder</span>

ncurses\_bottom\_panel
======================

Moves a visible panel to the bottom of the stack

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_bottom\_panel</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

ncurses\_can\_change\_color
===========================

Checks if terminal color definitions can be changed

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_can\_change\_color</span> ( <span
class="methodparam">void</span> )

Checks whether the terminal has color capabilities and whether the
programmer can change color definitions using <span
class="function">ncurses\_init\_color</span>. ncurses must be
initialized using <span class="function">ncurses\_init</span> before
calling this function.

### 参数

此函数没有参数。

### 返回值

Return **`true`** if the programmer can change color definitions,
**`false`** otherwise.

### 参见

-   <span class="function">ncurses\_has\_colors</span>
-   <span class="function">ncurses\_init\_color</span>
-   <span class="function">ncurses\_start\_color</span>

ncurses\_cbreak
===============

Switch off input buffering

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_cbreak</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Disables line buffering and character processing (interrupt and flow
control characters are unaffected), making characters typed by the user
immediately available to the program.

### 返回值

Returns **`true`** or **`NCURSES_ERR`** if any error occurred.

### 参见

-   <span class="function">ncurses\_nocbreak</span>

ncurses\_clear
==============

Clear screen

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_clear</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Clears the screen completely without setting blanks.

Note: <span class="function">ncurses\_clear</span> clears the screen
without setting blanks, which have the current background rendition. To
clear screen with blanks, use <span
class="function">ncurses\_erase</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ncurses\_erase</span>

ncurses\_clrtobot
=================

Clear screen from current position to bottom

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_clrtobot</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Erases all lines from cursor to end of screen and creates blanks. Blanks
created by <span class="function">ncurses\_clrtobot</span> have the
current background rendition.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ncurses\_clear</span>
-   <span class="function">ncurses\_clrtoeol</span>

ncurses\_clrtoeol
=================

Clear screen from current position to end of line

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_clrtoeol</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Erases the current line from cursor position to the end. Blanks created
by <span class="function">ncurses\_clrtoeol</span> have the current
background rendition.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ncurses\_clear</span>
-   <span class="function">ncurses\_clrtobot</span>

ncurses\_color\_content
=======================

Retrieves RGB components of a color

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_color\_content</span> ( <span
class="methodparam"><span class="type">int</span> `$color`</span> ,
<span class="methodparam"><span class="type">int</span> `&$r`</span> ,
<span class="methodparam"><span class="type">int</span> `&$g`</span> ,
<span class="methodparam"><span class="type">int</span> `&$b`</span> )

Retrieves the red, green, and blue components for the given color
definition. Terminal color capabilities must be initialized with <span
class="function">ncurses\_start\_color</span> prior to calling this
function.

### 参数

`color`  
The number of the color to retrieve information for. May be one of the
pre-defined color constants.

`r`  
A reference to which to return the red component of the color. The value
returned to the reference will be between 0 and 1000.

`g`  
A reference to which to return the green component of the color. The
value returned to the reference will be between 0 and 1000.

`b`  
A reference to which to return the blue component of the color. The
value returned to the reference will be between 0 and 1000.

### 返回值

Returns *-1* if the function was successful, and *0* if ncurses or
terminal color capabilities have not been initialized.

### 参见

-   <span class="function">ncurses\_init\_color</span>
-   <span class="function">ncurses\_start\_color</span>

ncurses\_color\_set
===================

Set active foreground and background colors

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_color\_set</span> ( <span
class="methodparam"><span class="type">int</span> `$pair`</span> )

Sets the active foreground and background colors. Any characters written
after this function is invoked will have these colors. This function
requires terminal colors to be supported and initialized using <span
class="function">ncurses\_start\_color</span> beforehand.

ncurses uses color pairs to specify both foreground and background
colors. Use <span class="function">ncurses\_init\_pair</span> to define
a color pair.

### 参数

`pair`  
The color pair from which to get the foreground and background colors to
set as the active colors.

### 返回值

Returns *-1* on success, and *0* on failure.

### 范例

**示例 \#1 Writing a string with a specified color to the screen**

``` php
<?php
ncurses_init();

// If the terminal supports colors, initialize and set active color
if (ncurses_has_colors()) {
    ncurses_start_color();
    ncurses_init_pair(1, NCURSES_COLOR_YELLOW, NCURSES_COLOR_BLUE);
    ncurses_color_set(1);
}

// Write a string at specified location
ncurses_mvaddstr(10, 10, "Hello world! Yellow on blue text!");

// Flush output to screen
ncurses_refresh();

ncurses_end();
?>
```

### 参见

-   <span class="function">ncurses\_init\_pair</span>
-   <span class="function">ncurses\_start\_color</span>

ncurses\_curs\_set
==================

Set cursor state

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_curs\_set</span> ( <span
class="methodparam"><span class="type">int</span> `$visibility`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`visibility`  

ncurses\_def\_prog\_mode
========================

Saves terminals (program) mode

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_def\_prog\_mode</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Saves the current terminal modes for program (in curses) for use by
<span class="function">ncurses\_reset\_prog\_mode</span>.

### 返回值

Returns **`false`** on success, otherwise **`true`**.

### 参见

-   <span class="function">ncurses\_reset\_prog\_mode</span>

ncurses\_def\_shell\_mode
=========================

Saves terminals (shell) mode

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_def\_shell\_mode</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Saves the current terminal modes for shell (not in curses) for use by
<span class="function">ncurses\_reset\_shell\_mode</span>.

### 返回值

Returns **`false`** on success, **`true`** otherwise.

### 参见

-   <span class="function">ncurses\_reset\_shell\_mode</span>

ncurses\_define\_key
====================

Define a keycode

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_define\_key</span> ( <span
class="methodparam"><span class="type">string</span>
`$definition`</span> , <span class="methodparam"><span
class="type">int</span> `$keycode`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`definition`  

`keycode`  

ncurses\_del\_panel
===================

Remove panel from the stack and delete it (but not the associated
window)

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_del\_panel</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

ncurses\_delay\_output
======================

Delay output on terminal using padding characters

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_delay\_output</span> ( <span
class="methodparam"><span class="type">int</span> `$milliseconds`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`milliseconds`  

ncurses\_delch
==============

Delete character at current position, move rest of line left

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_delch</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Deletes the character under the cursor. All characters to the right of
the cursor on the same line are moved to the left one position and the
last character on the line is filled with a blank. The cursor position
does not change.

### 返回值

Returns **`false`** on success, **`true`** otherwise.

### 参见

-   <span class="function">ncurses\_deleteln</span>

ncurses\_deleteln
=================

Delete line at current position, move rest of screen up

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_deleteln</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Deletes the current line under cursor position. All lines below the
current line are moved up one line. The bottom line of window is
cleared. Cursor position does not change.

### 返回值

Returns **`false`** on success, otherwise **`true`**.

### 参见

-   <span class="function">ncurses\_delch</span>

ncurses\_delwin
===============

Delete a ncurses window

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_delwin</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_doupdate
=================

Write all prepared refreshes to terminal

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_doupdate</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Compares the virtual screen to the physical screen and updates the
physical screen. This way is more effective than using multiple refresh
calls.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

ncurses\_echo
=============

Activate keyboard input echo

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_echo</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Enables echo mode. All characters typed by user are echoed by <span
class="function">ncurses\_getch</span>.

### 返回值

Returns **`false`** on success, **`true`** if any error occurred.

### 参见

-   <span class="function">ncurses\_noecho</span> to disable echo mode

ncurses\_echochar
=================

Single character output including refresh

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_echochar</span> ( <span
class="methodparam"><span class="type">int</span> `$character`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`character`  

ncurses\_end
============

Stop using ncurses, clean up the screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_end</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_erase
==============

Erase terminal screen

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_erase</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Fills the terminal screen with blanks.

Created blanks have the current background rendition, set by <span
class="function">ncurses\_bkgd</span>.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 参见

-   <span class="function">ncurses\_bkgd</span>
-   <span class="function">ncurses\_clear</span>

ncurses\_erasechar
==================

Returns current erase character

### 说明

<span class="type">string</span> <span
class="methodname">ncurses\_erasechar</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the current erase character.

### 返回值

The current erase char, as a string.

### 参见

-   <span class="function">ncurses\_killchar</span>

ncurses\_filter
===============

Set LINES for iniscr() and newterm() to 1

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_filter</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_flash
==============

Flash terminal screen (visual bell)

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_flash</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Flashes the screen, and if its not possible, sends an audible alert
(bell).

### 返回值

Returns **`false`** on success, otherwise **`true`**.

### 参见

-   <span class="function">ncurses\_beep</span>

ncurses\_flushinp
=================

Flush keyboard input buffer

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_flushinp</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Throws away any typeahead that has been typed and has not yet been read
by your program.

### 返回值

Returns **`false`** on success, otherwise **`true`**.

ncurses\_getch
==============

Read a character from keyboard

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_getch</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_getmaxyx
=================

Returns the size of a window

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_getmaxyx</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span> `&$y`</span> ,
<span class="methodparam"><span class="type">int</span> `&$x`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Gets the horizontal and vertical size of the given `window` into the
given variables.

Variables must be passed as reference, so they are updated when the user
changes the terminal size.

### 参数

`window`  
The measured window

`y`  
This will be set to the window height

`x`  
This will be set to the window width

### 返回值

没有返回值。

ncurses\_getmouse
=================

Reads mouse event

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_getmouse</span> ( <span
class="methodparam"><span class="type">array</span> `&$mevent`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

<span class="function">ncurses\_getmouse</span> reads mouse event out of
queue.

### 参数

`mevent`  
Event options will be delivered in this parameter which has to be an
array, passed by reference (see example below).

On success an associative array with following keys will be delivered:

-   "id" : Id to distinguish multiple devices

-   "x" : screen relative x-position in character cells

-   "y" : screen relative y-position in character cells

-   "z" : currently not supported

-   "mmask" : Mouse action

### 返回值

Returns **`false`** if a mouse event is actually visible in the given
window, otherwise returns **`true`**.

### 范例

**示例 \#1 <span class="function">ncurses\_getmouse</span> example**

``` php
<?php
switch (ncurses_getch()){
  case NCURSES_KEY_MOUSE:
    if (!ncurses_getmouse($mevent)){
      if ($mevent["mmask"] & NCURSES_MOUSE_BUTTON1_PRESSED){
        $mouse_x = $mevent["x"]; // Save mouse position
        $mouse_y = $mevent["y"];
      }
    }
  break;

  default:
    /* .... */
}
?>
```

### 参见

-   <span class="function">ncurses\_ungetmouse</span>

ncurses\_getyx
==============

Returns the current cursor position for a window

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_getyx</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span> `&$y`</span> ,
<span class="methodparam"><span class="type">int</span> `&$x`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`y`  

`x`  

ncurses\_halfdelay
==================

Put terminal into halfdelay mode

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_halfdelay</span> ( <span
class="methodparam"><span class="type">int</span> `$tenth`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`tenth`  

ncurses\_has\_colors
====================

Checks if terminal has color capabilities

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_has\_colors</span> ( <span
class="methodparam">void</span> )

Checks whether the terminal has color capabilities. This function can be
used to write terminal-independent programs. ncurses must be initialized
using <span class="function">ncurses\_init</span> before calling this
function.

### 参数

此函数没有参数。

### 返回值

Return **`true`** if the terminal has color capabilities, **`false`**
otherwise.

### 范例

**示例 \#1 Writing a string with a specified color to the screen**

``` php
<?php
ncurses_init();

// If the terminal supports colors, initialize and set active color
if (ncurses_has_colors()) {
    ncurses_start_color();
    ncurses_init_pair(1, NCURSES_COLOR_YELLOW, NCURSES_COLOR_BLUE);
    ncurses_color_set(1);
}

// Write a string at specified location
ncurses_mvaddstr(10, 10, "Hello world! Yellow on blue text!");

// Flush output to screen
ncurses_refresh();

ncurses_end();
?>
```

### 参见

-   <span class="function">ncurses\_can\_change\_color</span>
-   <span class="function">ncurses\_start\_color</span>

ncurses\_has\_ic
================

Check for insert- and delete-capabilities

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_has\_ic</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Checks whether the terminal has insert and delete capabilities.

### 返回值

Returns **`true`** if the terminal has insert/delete-capabilities,
**`false`** otherwise.

### 参见

-   <span class="function">ncurses\_has\_il</span>

ncurses\_has\_il
================

Check for line insert- and delete-capabilities

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_has\_il</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Checks whether the terminal has insert- and delete-line-capabilities.

### 返回值

Returns **`true`** if the terminal has insert/delete-line capabilities,
**`false`** otherwise.

### 参见

-   <span class="function">ncurses\_has\_ic</span>

ncurses\_has\_key
=================

Check for presence of a function key on terminal keyboard

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_has\_key</span> ( <span
class="methodparam"><span class="type">int</span> `$keycode`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`keycode`  

ncurses\_hide\_panel
====================

Remove panel from the stack, making it invisible

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_hide\_panel</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

ncurses\_hline
==============

Draw a horizontal line at current position using an attributed character
and max. n characters long

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_hline</span> ( <span
class="methodparam"><span class="type">int</span> `$charattr`</span> ,
<span class="methodparam"><span class="type">int</span> `$n`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`charattr`  

`n`  

ncurses\_inch
=============

Get character and attribute at current position

### 说明

<span class="type">string</span> <span
class="methodname">ncurses\_inch</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the character from the current position.

### 返回值

Returns the character, as a string.

ncurses\_init\_color
====================

Define a terminal color

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_init\_color</span> ( <span
class="methodparam"><span class="type">int</span> `$color`</span> ,
<span class="methodparam"><span class="type">int</span> `$r`</span> ,
<span class="methodparam"><span class="type">int</span> `$g`</span> ,
<span class="methodparam"><span class="type">int</span> `$b`</span> )

Defines or redefines the given color. When this function is called, all
occurrences of the given color on the screen, if any, immediately change
to the new definition.

Color capabilities must be supported by the terminal and initialized
using <span class="function">ncurses\_start\_color</span> prior to
calling this function. In addition, the terminal must have color
changing capabilities; use <span
class="function">ncurses\_can\_change\_color</span> to check for this.

### 参数

`color`  
The identification number of the color to redefine. It may be one of the
default color constants.

`r`  
A color value, between 0 and 1000, for the red component.

`g`  
A color value, between 0 and 1000, for the green component.

`b`  
A color value, between 0 and 1000, for the blue component.

### 返回值

Returns *-1* if the function was successful, and *0* if ncurses or
terminal color capabilities have not been initialized or the terminal
does not have color changing capabilities.

### 参见

-   <span class="function">ncurses\_color\_content</span>
-   <span class="function">ncurses\_start\_color</span>

ncurses\_init\_pair
===================

Define a color pair

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_init\_pair</span> ( <span
class="methodparam"><span class="type">int</span> `$pair`</span> , <span
class="methodparam"><span class="type">int</span> `$fg`</span> , <span
class="methodparam"><span class="type">int</span> `$bg`</span> )

Defines or redefines the given color pair to have the given foreground
and background colors. If the color pair was previously initialized, the
screen is refreshed and all occurrences of it are changed to reflect the
new definition.

Color capabilities must be initialized using <span
class="function">ncurses\_start\_color</span> before calling this
function. The first color pair (color pair *0*) is assumed to be white
on black by default, but can be changed using <span
class="function">ncurses\_assume\_default\_colors</span>.

### 参数

`pair`  
The number of the color pair to define.

`fg`  
The foreground color for the color pair. May be one of the
<a href="/ncurses/constants.html#Colors" class="link">pre-defined colors</a>
or one defined by <span class="function">ncurses\_init\_color</span> if
the terminal has color changing capabilities.

`bg`  
The background color for the color pair. May be one of the
<a href="/ncurses/constants.html#Colors" class="link">pre-defined colors</a>
or one defined by <span class="function">ncurses\_init\_color</span> if
the terminal has color changing capabilities.

### 返回值

Returns *-1* if the function was successful, and *0* if ncurses or color
support were not initialized.

### 注释

Note that color changing capabilities are not required for defining
color pairs of pre-existing colors, but only for changing definitions
(red, green, and blue components) of colors themselves per <span
class="function">ncurses\_init\_color</span>.

### 范例

**示例 \#1 Writing a string with a specified color to the screen**

``` php
<?php
ncurses_init();

// If the terminal supports colors, initialize and set active color
if (ncurses_has_colors()) {
    ncurses_start_color();
    ncurses_init_pair(1, NCURSES_COLOR_YELLOW, NCURSES_COLOR_BLUE);
    ncurses_color_set(1);
}

// Write a string at specified location
ncurses_mvaddstr(10, 10, "Hello world! Yellow on blue text!");

// Flush output to screen
ncurses_refresh();

ncurses_end();
?>
```

### 参见

-   <span class="function">ncurses\_pair\_content</span>
-   <span class="function">ncurses\_start\_color</span>

ncurses\_init
=============

Initialize ncurses

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_init</span> ( <span
class="methodparam">void</span> )

Initializes the ncurses interface. This function must be used before any
other ncurses function call.

Note that <span class="function">ncurses\_end</span> must be called
before exiting from the program, or the terminal will not be restored to
its proper non-visual mode.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="function">ncurses\_end</span>

ncurses\_insch
==============

Insert character moving rest of line including character at current
position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_insch</span> ( <span
class="methodparam"><span class="type">int</span> `$character`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`character`  

ncurses\_insdelln
=================

Insert lines before current line scrolling down (negative numbers delete
and scroll up)

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_insdelln</span> ( <span
class="methodparam"><span class="type">int</span> `$count`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`count`  

ncurses\_insertln
=================

Insert a line, move rest of screen down

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_insertln</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Inserts a new line above the current line. The bottom line will be lost.

ncurses\_insstr
===============

Insert string at current position, moving rest of line right

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_insstr</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`text`  

ncurses\_instr
==============

Reads string from terminal screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_instr</span> ( <span
class="methodparam"><span class="type">string</span> `&$buffer`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Reads a string from the terminal screen and returns the number of
characters read from the current character position until end of line.

### 参数

`buffer`  
The characters. Attributes will be stripped.

### 返回值

Returns the number of characters.

ncurses\_isendwin
=================

Ncurses is in endwin mode, normal screen output may be performed

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_isendwin</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Checks if ncurses is in endwin mode.

### 返回值

Returns **`true`**, if <span class="function">ncurses\_end</span> has
been called without any subsequent calls to <span
class="function">ncurses\_wrefresh</span>, **`false`** otherwise.

### 参见

-   <span class="function">ncurses\_end</span>
-   <span class="function">ncurses\_wrefresh</span>

ncurses\_keyok
==============

Enable or disable a keycode

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_keyok</span> ( <span
class="methodparam"><span class="type">int</span> `$keycode`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$enable`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`keycode`  

`enable`  

ncurses\_keypad
===============

Turns keypad on or off

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_keypad</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">bool</span> `$bf`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`bf`  

ncurses\_killchar
=================

Returns current line kill character

### 说明

<span class="type">string</span> <span
class="methodname">ncurses\_killchar</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the current line kill character.

### 返回值

Returns the kill character, as a string.

### 参见

-   <span class="function">ncurses\_erasechar</span>

ncurses\_longname
=================

Returns terminals description

### 说明

<span class="type">string</span> <span
class="methodname">ncurses\_longname</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns a verbose description of the terminal.

### 返回值

Returns the description, as a string truncated to 128 characters. On
errors, returns **`null`**.

### 参见

-   <span class="function">ncurses\_termname</span>

ncurses\_meta
=============

Enables/Disable 8-bit meta key information

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_meta</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">bool</span>
`$8bit`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`8bit`  

ncurses\_mouse\_trafo
=====================

Transforms coordinates

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_mouse\_trafo</span> ( <span
class="methodparam"><span class="type">int</span> `&$y`</span> , <span
class="methodparam"><span class="type">int</span> `&$x`</span> , <span
class="methodparam"><span class="type">bool</span> `$toscreen`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

`toscreen`  

ncurses\_mouseinterval
======================

Set timeout for mouse button clicks

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mouseinterval</span> ( <span
class="methodparam"><span class="type">int</span> `$milliseconds`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`milliseconds`  

ncurses\_mousemask
==================

Sets mouse options

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mousemask</span> ( <span
class="methodparam"><span class="type">int</span> `$newmask`</span> ,
<span class="methodparam"><span class="type">int</span>
`&$oldmask`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Sets mouse events to be reported. By default no mouse events will be
reported.

Mouse events are represented by **`NCURSES_KEY_MOUSE`** in the <span
class="function">ncurses\_wgetch</span> input stream. To read the event
data and pop the event of queue, call <span
class="function">ncurses\_getmouse</span>.

### 参数

`newmask`  
Mouse mask options can be set with the following predefined constants:

-   NCURSES\_BUTTON1\_PRESSED

-   NCURSES\_BUTTON1\_RELEASED

-   NCURSES\_BUTTON1\_CLICKED

-   NCURSES\_BUTTON1\_DOUBLE\_CLICKED

-   NCURSES\_BUTTON1\_TRIPLE\_CLICKED

-   NCURSES\_BUTTON2\_PRESSED

-   NCURSES\_BUTTON2\_RELEASED

-   NCURSES\_BUTTON2\_CLICKED

-   NCURSES\_BUTTON2\_DOUBLE\_CLICKED

-   NCURSES\_BUTTON2\_TRIPLE\_CLICKED

-   NCURSES\_BUTTON3\_PRESSED

-   NCURSES\_BUTTON3\_RELEASED

-   NCURSES\_BUTTON3\_CLICKED

-   NCURSES\_BUTTON3\_DOUBLE\_CLICKED

-   NCURSES\_BUTTON3\_TRIPLE\_CLICKED

-   NCURSES\_BUTTON4\_PRESSED

-   NCURSES\_BUTTON4\_RELEASED

-   NCURSES\_BUTTON4\_CLICKED

-   NCURSES\_BUTTON4\_DOUBLE\_CLICKED

-   NCURSES\_BUTTON4\_TRIPLE\_CLICKED

-   NCURSES\_BUTTON\_SHIFT\>

-   NCURSES\_BUTTON\_CTRL

-   NCURSES\_BUTTON\_ALT

-   NCURSES\_ALL\_MOUSE\_EVENTS

-   NCURSES\_REPORT\_MOUSE\_POSITION

As a side effect, setting a zero mousemask in `newmask` turns off the
mouse pointer. Setting a non zero value turns mouse pointer on.

`oldmask`  
This will be set to the previous value of the mouse event mask.

### 返回值

Returns the mask of reportable events. On complete failure, it returns
*0*.

### 范例

**示例 \#1 <span class="function">ncurses\_mousemask</span> example**

``` php
<?php
$newmask = NCURSES_BUTTON1_CLICKED + NCURSES_BUTTON1_RELEASED;
$mask = ncurses_mousemask($newmask, $oldmask);
if ($mask & $newmask){
    printf("All specified mouse options will be supported\n");
}
?>
```

### 参见

-   <span class="function">ncurses\_getch</span>
-   <span class="function">ncurses\_getmouse</span>
-   <span class="function">ncurses\_ungetmouse</span>

ncurses\_move\_panel
====================

Moves a panel so that its upper-left corner is at \[startx, starty\]

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_move\_panel</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> ,
<span class="methodparam"><span class="type">int</span> `$startx`</span>
, <span class="methodparam"><span class="type">int</span>
`$starty`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

`startx`  

`starty`  

ncurses\_move
=============

Move output position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_move</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

ncurses\_mvaddch
================

Move current position and add character

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvaddch</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">int</span> `$c`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

`c`  

ncurses\_mvaddchnstr
====================

Move position and add attributed string with specified length

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvaddchnstr</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">string</span> `$s`</span> , <span
class="methodparam"><span class="type">int</span> `$n`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

`s`  

`n`  

ncurses\_mvaddchstr
===================

Move position and add attributed string

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvaddchstr</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">string</span> `$s`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

`s`  

ncurses\_mvaddnstr
==================

Move position and add string with specified length

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvaddnstr</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">string</span> `$s`</span> , <span
class="methodparam"><span class="type">int</span> `$n`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

`s`  

`n`  

ncurses\_mvaddstr
=================

Move position and add string

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvaddstr</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">string</span> `$s`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

`s`  

ncurses\_mvcur
==============

Move cursor immediately

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvcur</span> ( <span
class="methodparam"><span class="type">int</span> `$old_y`</span> ,
<span class="methodparam"><span class="type">int</span> `$old_x`</span>
, <span class="methodparam"><span class="type">int</span>
`$new_y`</span> , <span class="methodparam"><span
class="type">int</span> `$new_x`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`old_y`  

`old_x`  

`new_y`  

`new_x`  

ncurses\_mvdelch
================

Move position and delete character, shift rest of line left

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvdelch</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

ncurses\_mvgetch
================

Move position and get character at new position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvgetch</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

ncurses\_mvhline
================

Set new position and draw a horizontal line using an attributed
character and max. n characters long

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvhline</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">int</span> `$attrchar`</span> ,
<span class="methodparam"><span class="type">int</span> `$n`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

`attrchar`  

`n`  

ncurses\_mvinch
===============

Move position and get attributed character at new position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvinch</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

ncurses\_mvvline
================

Set new position and draw a vertical line using an attributed character
and max. n characters long

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvvline</span> ( <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> , <span
class="methodparam"><span class="type">int</span> `$attrchar`</span> ,
<span class="methodparam"><span class="type">int</span> `$n`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`y`  

`x`  

`attrchar`  

`n`  

ncurses\_mvwaddstr
==================

Add string at new position in window

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_mvwaddstr</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span> `$y`</span> ,
<span class="methodparam"><span class="type">int</span> `$x`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`y`  

`x`  

`text`  

ncurses\_napms
==============

Sleep

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_napms</span> ( <span
class="methodparam"><span class="type">int</span> `$milliseconds`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`milliseconds`  

ncurses\_new\_panel
===================

Create a new panel and associate it with window

### 说明

<span class="type">resource</span> <span
class="methodname">ncurses\_new\_panel</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_newpad
===============

Creates a new pad (window)

### 说明

<span class="type">resource</span> <span
class="methodname">ncurses\_newpad</span> ( <span
class="methodparam"><span class="type">int</span> `$rows`</span> , <span
class="methodparam"><span class="type">int</span> `$cols`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`rows`  

`cols`  

ncurses\_newwin
===============

Create a new window

### 说明

<span class="type">resource</span> <span
class="methodname">ncurses\_newwin</span> ( <span
class="methodparam"><span class="type">int</span> `$rows`</span> , <span
class="methodparam"><span class="type">int</span> `$cols`</span> , <span
class="methodparam"><span class="type">int</span> `$y`</span> , <span
class="methodparam"><span class="type">int</span> `$x`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Creates a new window to draw elements in.

When creating additional windows, remember to use <span
class="function">ncurses\_getmaxyx</span> to check for available space,
as terminal size is individual and may vary.

### 参数

`rows`  
Number of rows

`cols`  
Number of columns

`y`  
y-coordinate of the origin

`x`  
x-coordinate of the origin

### 返回值

Returns a resource ID for the new window.

ncurses\_nl
===========

Translate newline and carriage return / line feed

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_nl</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_nocbreak
=================

Switch terminal to cooked mode

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_nocbreak</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns terminal to normal (cooked) mode. Initially the terminal may or
may not be in cbreak mode as the mode is inherited. Therefore a program
should call <span class="function">ncurses\_cbreak</span> and <span
class="function">ncurses\_nocbreak</span> explicitly.

### 返回值

Returns **`true`** if any error occurred, otherwise **`false`**.

### 参见

-   <span class="function">ncurses\_cbreak</span>

ncurses\_noecho
===============

Switch off keyboard input echo

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_noecho</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Prevents echoing of user typed characters.

### 返回值

Returns **`true`** if any error occurred, **`false`** otherwise.

### 参见

-   <span class="function">ncurses\_echo</span>
-   <span class="function">ncurses\_getch</span>

ncurses\_nonl
=============

Do not translate newline and carriage return / line feed

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_nonl</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_noqiflush
==================

Do not flush on signal characters

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_noqiflush</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_noraw
==============

Switch terminal out of raw mode

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_noraw</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Switches the terminal out of raw mode. Raw mode is similar to cbreak
mode, in that characters typed are immediately passed through to the
user program. The difference is that in raw mode, the interrupt, quit,
suspend and flow control characters are all passed through
uninterpreted, instead of generating a signal.

### 返回值

Returns **`true`** if any error occurred, otherwise **`false`**.

### 参见

-   <span class="function">ncurses\_raw</span>
-   <span class="function">ncurses\_cbreak</span>
-   <span class="function">ncurses\_nocbreak</span>

ncurses\_pair\_content
======================

Retrieves foreground and background colors of a color pair

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_pair\_content</span> ( <span
class="methodparam"><span class="type">int</span> `$pair`</span> , <span
class="methodparam"><span class="type">int</span> `&$f`</span> , <span
class="methodparam"><span class="type">int</span> `&$b`</span> )

Retrieves the foreground and background colors that constitute the given
color pair. Terminal color capabilities must be initialized with <span
class="function">ncurses\_start\_color</span> prior to calling this
function.

### 参数

`pair`  
The number of the color pair to retrieve information for.

`f`  
A reference to which to return the foreground color of the color pair.
The information returned will be a color number referring to one of the
<a href="/ncurses/constants.html#Colors" class="link">pre-defined colors</a>
or a color defined previously by <span
class="function">ncurses\_init\_color</span> if the terminal supports
color changing.

`b`  
A reference to which to return the background color of the color pair.
The information returned will be a color number referring to one of the
<a href="/ncurses/constants.html#Colors" class="link">pre-defined colors</a>
or a color defined previously by <span
class="function">ncurses\_init\_color</span> if the terminal supports
color changing.

### 返回值

Returns *-1* if the function was successful, and *0* if ncurses or
terminal color capabilities have not been initialized.

### 参见

-   <span class="function">ncurses\_init\_pair</span>
-   <span class="function">ncurses\_start\_color</span>

ncurses\_panel\_above
=====================

Returns the panel above panel

### 说明

<span class="type">resource</span> <span
class="methodname">ncurses\_panel\_above</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

### 返回值

If panel is null, returns the bottom panel in the stack.

ncurses\_panel\_below
=====================

Returns the panel below panel

### 说明

<span class="type">resource</span> <span
class="methodname">ncurses\_panel\_below</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

### 参数

If panel is null, returns the top panel in the stack.

ncurses\_panel\_window
======================

Returns the window associated with panel

### 说明

<span class="type">resource</span> <span
class="methodname">ncurses\_panel\_window</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

ncurses\_pnoutrefresh
=====================

Copies a region from a pad into the virtual screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_pnoutrefresh</span> ( <span
class="methodparam"><span class="type">resource</span> `$pad`</span> ,
<span class="methodparam"><span class="type">int</span>
`$pminrow`</span> , <span class="methodparam"><span
class="type">int</span> `$pmincol`</span> , <span
class="methodparam"><span class="type">int</span> `$sminrow`</span> ,
<span class="methodparam"><span class="type">int</span>
`$smincol`</span> , <span class="methodparam"><span
class="type">int</span> `$smaxrow`</span> , <span
class="methodparam"><span class="type">int</span> `$smaxcol`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`pad`  

`pminrow`  

`pmincol`  

`sminrow`  

`smincol`  

`smaxrow`  

`smaxcol`  

ncurses\_prefresh
=================

Copies a region from a pad into the virtual screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_prefresh</span> ( <span
class="methodparam"><span class="type">resource</span> `$pad`</span> ,
<span class="methodparam"><span class="type">int</span>
`$pminrow`</span> , <span class="methodparam"><span
class="type">int</span> `$pmincol`</span> , <span
class="methodparam"><span class="type">int</span> `$sminrow`</span> ,
<span class="methodparam"><span class="type">int</span>
`$smincol`</span> , <span class="methodparam"><span
class="type">int</span> `$smaxrow`</span> , <span
class="methodparam"><span class="type">int</span> `$smaxcol`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`pad`  

`pminrow`  

`pmincol`  

`sminrow`  

`smincol`  

`smaxrow`  

`smaxcol`  

ncurses\_putp
=============

Apply padding information to the string and output it

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_putp</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`text`  

ncurses\_qiflush
================

Flush on signal characters

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_qiflush</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_raw
============

Switch terminal into raw mode

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_raw</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Places the terminal in raw mode. Raw mode is similar to cbreak mode, in
that characters typed are immediately passed through to the user
program. The difference is that in raw mode, the interrupt, quit,
suspend and flow control characters are all passed through
uninterpreted, instead of generating a signal.

### 返回值

Returns **`true`** if any error occurred, otherwise **`false`**.

### 参见

-   <span class="function">ncurses\_noraw</span>
-   <span class="function">ncurses\_cbreak</span>
-   <span class="function">ncurses\_nocbreak</span>

ncurses\_refresh
================

Refresh screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_refresh</span> ( <span
class="methodparam"><span class="type">int</span> `$ch`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`ch`  

ncurses\_replace\_panel
=======================

Replaces the window associated with panel

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_replace\_panel</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$window`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

`window`  

ncurses\_reset\_prog\_mode
==========================

Resets the prog mode saved by def\_prog\_mode

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_reset\_prog\_mode</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_reset\_shell\_mode
===========================

Resets the shell mode saved by def\_shell\_mode

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_reset\_shell\_mode</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_resetty
================

Restores saved terminal state

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_resetty</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Restores the terminal state, which was previously saved by calling <span
class="function">ncurses\_savetty</span>.

### 返回值

Always returns **`false`**.

### 参见

-   <span class="function">ncurses\_savetty</span>

ncurses\_savetty
================

Saves terminal state

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_savetty</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Saves the current terminal state. The saved terminal state can be
restored with <span class="function">ncurses\_resetty</span>.

### 返回值

Always returns **`false`**.

### 参见

-   <span class="function">ncurses\_resetty</span>

ncurses\_scr\_dump
==================

Dump screen content to file

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_scr\_dump</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`filename`  

ncurses\_scr\_init
==================

Initialize screen from file dump

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_scr\_init</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`filename`  

ncurses\_scr\_restore
=====================

Restore screen from file dump

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_scr\_restore</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`filename`  

ncurses\_scr\_set
=================

Inherit screen from file dump

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_scr\_set</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`filename`  

ncurses\_scrl
=============

Scroll window content up or down without changing current position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_scrl</span> ( <span
class="methodparam"><span class="type">int</span> `$count`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`count`  

ncurses\_show\_panel
====================

Places an invisible panel on top of the stack, making it visible

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_show\_panel</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

ncurses\_slk\_attr
==================

Returns current soft label key attribute

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_slk\_attr</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns the current soft label key attribute.

### 返回值

The attribute, as an integer.

ncurses\_slk\_attroff
=====================

Turn off the given attributes for soft function-key labels

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_slk\_attroff</span> ( <span
class="methodparam"><span class="type">int</span> `$intarg`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`intarg`  

ncurses\_slk\_attron
====================

Turn on the given attributes for soft function-key labels

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_slk\_attron</span> ( <span
class="methodparam"><span class="type">int</span> `$intarg`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`intarg`  

ncurses\_slk\_attrset
=====================

Set given attributes for soft function-key labels

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_slk\_attrset</span> ( <span
class="methodparam"><span class="type">int</span> `$intarg`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`intarg`  

ncurses\_slk\_clear
===================

Clears soft labels from screen

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_slk\_clear</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

The function <span class="function">ncurses\_slk\_clear</span> clears
soft label keys from screen.

### 返回值

Returns **`true`** on errors, **`false`** otherwise.

ncurses\_slk\_color
===================

Sets color for soft label keys

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_slk\_color</span> ( <span
class="methodparam"><span class="type">int</span> `$intarg`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`intarg`  

ncurses\_slk\_init
==================

Initializes soft label key functions

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_slk\_init</span> ( <span
class="methodparam"><span class="type">int</span> `$format`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Initializes soft label key functions

This function must be called before <span
class="function">ncurses\_init</span> or <span
class="function">ncurses\_newwin</span> is called.

### 参数

`format`  
If <span class="function">ncurses\_init</span> eventually uses a line
from stdscr to emulate the soft labels, then this parameter determines
how the labels are arranged of the screen.

0 indicates a 3-2-3 arrangement of the labels, 1 indicates a 4-4
arrangement and 2 indicates the PC like 4-4-4 mode, but in addition an
index line will be created.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

ncurses\_slk\_noutrefresh
=========================

Copies soft label keys to virtual screen

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_slk\_noutrefresh</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_slk\_refresh
=====================

Copies soft label keys to screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_slk\_refresh</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Copies soft label keys from virtual screen to physical screen.

ncurses\_slk\_restore
=====================

Restores soft label keys

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_slk\_restore</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Restores the soft label keys after <span
class="function">ncurses\_slk\_clear</span> has been performed.

ncurses\_slk\_set
=================

Sets function key labels

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_slk\_set</span> ( <span
class="methodparam"><span class="type">int</span> `$labelnr`</span> ,
<span class="methodparam"><span class="type">string</span>
`$label`</span> , <span class="methodparam"><span
class="type">int</span> `$format`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`labelnr`  

`label`  

`format`  

ncurses\_slk\_touch
===================

Forces output when ncurses\_slk\_noutrefresh is performed

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_slk\_touch</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Forces all the soft labels to be output the next time a <span
class="function">ncurses\_slk\_noutrefresh</span> is performed.

ncurses\_standend
=================

Stop using 'standout' attribute

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_standend</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_standout
=================

Start using 'standout' attribute

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_standout</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_start\_color
=====================

Initializes color functionality

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_start\_color</span> ( <span
class="methodparam">void</span> )

Initializes color functionality in ncurses. This function must be called
before any color manipulation functions are called and after <span
class="function">ncurses\_init</span> is called. It is good practice to
call this function right after <span
class="function">ncurses\_init</span>.

### 参数

此函数没有参数。

### 返回值

Returns *0* on success, or *-1* if the color table could not be
allocated or ncurses was not initialized.

### 范例

**示例 \#1 Writing a string with a specified color to the screen**

``` php
<?php
ncurses_init();

// If the terminal supports colors, initialize and set active color
if (ncurses_has_colors()) {
    ncurses_start_color();
    ncurses_init_pair(1, NCURSES_COLOR_YELLOW, NCURSES_COLOR_BLUE);
    ncurses_color_set(1);
}

// Write a string at specified location
ncurses_mvaddstr(10, 10, "Hello world! Yellow on blue text!");

// Flush output to screen
ncurses_refresh();

ncurses_end();
?>
```

### 参见

-   <span class="function">ncurses\_can\_change\_color</span>
-   <span class="function">ncurses\_has\_colors</span>

ncurses\_termattrs
==================

Returns a logical OR of all attribute flags supported by terminal

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_termattrs</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_termname
=================

Returns terminals (short)-name

### 说明

<span class="type">string</span> <span
class="methodname">ncurses\_termname</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Returns terminals shortname.

### 返回值

Returns the shortname of the terminal, truncated to 14 characters. On
errors, returns **`null`**.

### 参见

-   <span class="function">ncurses\_longname</span>

ncurses\_timeout
================

Set timeout for special key sequences

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_timeout</span> ( <span
class="methodparam"><span class="type">int</span> `$millisec`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`millisec`  

ncurses\_top\_panel
===================

Moves a visible panel to the top of the stack

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_top\_panel</span> ( <span
class="methodparam"><span class="type">resource</span> `$panel`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`panel`  

ncurses\_typeahead
==================

Specify different filedescriptor for typeahead checking

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_typeahead</span> ( <span
class="methodparam"><span class="type">int</span> `$fd`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`fd`  

ncurses\_ungetch
================

Put a character back into the input stream

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_ungetch</span> ( <span
class="methodparam"><span class="type">int</span> `$keycode`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`keycode`  

ncurses\_ungetmouse
===================

Pushes mouse event to queue

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_ungetmouse</span> ( <span
class="methodparam"><span class="type">array</span> `$mevent`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Pushes a KEY\_MOUSE event onto the input queue and associates with this
event the given state data and screen-relative character cell
coordinates, specified in `mevent`.

### 参数

`mevent`  
An associative array specifying the event options:

-   "id" : Id to distinguish multiple devices

-   "x" : screen relative x-position in character cells

-   "y" : screen relative y-position in character cells

-   "z" : currently not supported

-   "mmask" : Mouse action

### 返回值

Returns **`false`** on success, **`true`** otherwise.

### 参见

-   <span class="function">ncurses\_getmouse</span>

ncurses\_update\_panels
=======================

Refreshes the virtual screen to reflect the relations between panels in
the stack

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_update\_panels</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_use\_default\_colors
=============================

Assign terminal default colors to color id -1

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_use\_default\_colors</span> ( <span
class="methodparam">void</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

ncurses\_use\_env
=================

Control use of environment information about terminal size

### 说明

<span class="type">void</span> <span
class="methodname">ncurses\_use\_env</span> ( <span
class="methodparam"><span class="type">bool</span> `$flag`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`flag`  

ncurses\_use\_extended\_names
=============================

Control use of extended names in terminfo descriptions

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_use\_extended\_names</span> ( <span
class="methodparam"><span class="type">bool</span> `$flag`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`flag`  

ncurses\_vidattr
================

Display the string on the terminal in the video attribute mode

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_vidattr</span> ( <span
class="methodparam"><span class="type">int</span> `$intarg`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`intarg`  

ncurses\_vline
==============

Draw a vertical line at current position using an attributed character
and max. n characters long

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_vline</span> ( <span
class="methodparam"><span class="type">int</span> `$charattr`</span> ,
<span class="methodparam"><span class="type">int</span> `$n`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`charattr`  

`n`  

ncurses\_waddch
===============

Adds character at current position in a window and advance cursor

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_waddch</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span> `$ch`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`ch`  

ncurses\_waddstr
================

Outputs text at current postion in window

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_waddstr</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">string</span>
`$str`</span> \[, <span class="methodparam"><span
class="type">int</span> `$n`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`str`  

`n`  

ncurses\_wattroff
=================

Turns off attributes for a window

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wattroff</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span>
`$attrs`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`attrs`  

ncurses\_wattron
================

Turns on attributes for a window

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wattron</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span>
`$attrs`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`attrs`  

ncurses\_wattrset
=================

Set the attributes for a window

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wattrset</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span>
`$attrs`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`attrs`  

ncurses\_wborder
================

Draws a border around the window using attributed characters

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wborder</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span> `$left`</span>
, <span class="methodparam"><span class="type">int</span>
`$right`</span> , <span class="methodparam"><span
class="type">int</span> `$top`</span> , <span class="methodparam"><span
class="type">int</span> `$bottom`</span> , <span
class="methodparam"><span class="type">int</span> `$tl_corner`</span> ,
<span class="methodparam"><span class="type">int</span>
`$tr_corner`</span> , <span class="methodparam"><span
class="type">int</span> `$bl_corner`</span> , <span
class="methodparam"><span class="type">int</span> `$br_corner`</span> )

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

Draws the specified lines and corners around the passed `window`.

Use <span class="function">ncurses\_border</span> for borders around the
main window.

### 参数

Each parameter expects 0 to draw a line and 1 to skip it.

`window`  
The window on which we operate

`left`  

`right`  

`top`  

`bottom`  

`tl_corner`  
Top left corner

`tr_corner`  
Top right corner

`bl_corner`  
Bottom left corner

`br_corner`  
Bottom right corner

### 参见

-   <span class="function">ncurses\_border</span>

ncurses\_wclear
===============

Clears window

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wclear</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_wcolor\_set
====================

Sets windows color pairings

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wcolor\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span>
`$color_pair`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`color_pair`  

ncurses\_werase
===============

Erase window contents

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_werase</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_wgetch
===============

Reads a character from keyboard (window)

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wgetch</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_whline
===============

Draws a horizontal line in a window at current position using an
attributed character and max. n characters long

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_whline</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span>
`$charattr`</span> , <span class="methodparam"><span
class="type">int</span> `$n`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`charattr`  

`n`  

ncurses\_wmouse\_trafo
======================

Transforms window/stdscr coordinates

### 说明

<span class="type">bool</span> <span
class="methodname">ncurses\_wmouse\_trafo</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span> `&$y`</span> ,
<span class="methodparam"><span class="type">int</span> `&$x`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$toscreen`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`x`  

`y`  

`toscreen`  

ncurses\_wmove
==============

Moves windows output position

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wmove</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span> `$y`</span> ,
<span class="methodparam"><span class="type">int</span> `$x`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`y`  

`x`  

ncurses\_wnoutrefresh
=====================

Copies window to virtual screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wnoutrefresh</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_wrefresh
=================

Refresh window on terminal screen

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wrefresh</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

此函数是*实验性*的。此函数的表象，包括名称及其相关文档都可能在未来的 PHP
发布版本中未通知就被修改。使用本函数风险自担。

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_wstandend
==================

End standout mode for a window

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wstandend</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_wstandout
==================

Enter standout mode for a window

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wstandout</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

ncurses\_wvline
===============

Draws a vertical line in a window at current position using an
attributed character and max. n characters long

### 说明

<span class="type">int</span> <span
class="methodname">ncurses\_wvline</span> ( <span
class="methodparam"><span class="type">resource</span> `$window`</span>
, <span class="methodparam"><span class="type">int</span>
`$charattr`</span> , <span class="methodparam"><span
class="type">int</span> `$n`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`window`  

`charattr`  

`n`  

**目录**

-   [ncurses\_addch](/ref/ncurses.html#ncurses_addch) — Add character at
    current position and advance cursor
-   [ncurses\_addchnstr](/ref/ncurses.html#ncurses_addchnstr) — Add
    attributed string with specified length at current position
-   [ncurses\_addchstr](/ref/ncurses.html#ncurses_addchstr) — Add
    attributed string at current position
-   [ncurses\_addnstr](/ref/ncurses.html#ncurses_addnstr) — Add string
    with specified length at current position
-   [ncurses\_addstr](/ref/ncurses.html#ncurses_addstr) — Output text at
    current position
-   [ncurses\_assume\_default\_colors](/ref/ncurses.html#ncurses_assume_default_colors)
    — Define default colors for color 0
-   [ncurses\_attroff](/ref/ncurses.html#ncurses_attroff) — Turn off the
    given attributes
-   [ncurses\_attron](/ref/ncurses.html#ncurses_attron) — Turn on the
    given attributes
-   [ncurses\_attrset](/ref/ncurses.html#ncurses_attrset) — Set given
    attributes
-   [ncurses\_baudrate](/ref/ncurses.html#ncurses_baudrate) — Returns
    baudrate of terminal
-   [ncurses\_beep](/ref/ncurses.html#ncurses_beep) — Let the terminal
    beep
-   [ncurses\_bkgd](/ref/ncurses.html#ncurses_bkgd) — Set background
    property for terminal screen
-   [ncurses\_bkgdset](/ref/ncurses.html#ncurses_bkgdset) — Control
    screen background
-   [ncurses\_border](/ref/ncurses.html#ncurses_border) — Draw a border
    around the screen using attributed characters
-   [ncurses\_bottom\_panel](/ref/ncurses.html#ncurses_bottom_panel) —
    Moves a visible panel to the bottom of the stack
-   [ncurses\_can\_change\_color](/ref/ncurses.html#ncurses_can_change_color)
    — Checks if terminal color definitions can be changed
-   [ncurses\_cbreak](/ref/ncurses.html#ncurses_cbreak) — Switch off
    input buffering
-   [ncurses\_clear](/ref/ncurses.html#ncurses_clear) — Clear screen
-   [ncurses\_clrtobot](/ref/ncurses.html#ncurses_clrtobot) — Clear
    screen from current position to bottom
-   [ncurses\_clrtoeol](/ref/ncurses.html#ncurses_clrtoeol) — Clear
    screen from current position to end of line
-   [ncurses\_color\_content](/ref/ncurses.html#ncurses_color_content) —
    Retrieves RGB components of a color
-   [ncurses\_color\_set](/ref/ncurses.html#ncurses_color_set) — Set
    active foreground and background colors
-   [ncurses\_curs\_set](/ref/ncurses.html#ncurses_curs_set) — Set
    cursor state
-   [ncurses\_def\_prog\_mode](/ref/ncurses.html#ncurses_def_prog_mode)
    — Saves terminals (program) mode
-   [ncurses\_def\_shell\_mode](/ref/ncurses.html#ncurses_def_shell_mode)
    — Saves terminals (shell) mode
-   [ncurses\_define\_key](/ref/ncurses.html#ncurses_define_key) —
    Define a keycode
-   [ncurses\_del\_panel](/ref/ncurses.html#ncurses_del_panel) — Remove
    panel from the stack and delete it (but not the associated window)
-   [ncurses\_delay\_output](/ref/ncurses.html#ncurses_delay_output) —
    Delay output on terminal using padding characters
-   [ncurses\_delch](/ref/ncurses.html#ncurses_delch) — Delete character
    at current position, move rest of line left
-   [ncurses\_deleteln](/ref/ncurses.html#ncurses_deleteln) — Delete
    line at current position, move rest of screen up
-   [ncurses\_delwin](/ref/ncurses.html#ncurses_delwin) — Delete a
    ncurses window
-   [ncurses\_doupdate](/ref/ncurses.html#ncurses_doupdate) — Write all
    prepared refreshes to terminal
-   [ncurses\_echo](/ref/ncurses.html#ncurses_echo) — Activate keyboard
    input echo
-   [ncurses\_echochar](/ref/ncurses.html#ncurses_echochar) — Single
    character output including refresh
-   [ncurses\_end](/ref/ncurses.html#ncurses_end) — Stop using ncurses,
    clean up the screen
-   [ncurses\_erase](/ref/ncurses.html#ncurses_erase) — Erase terminal
    screen
-   [ncurses\_erasechar](/ref/ncurses.html#ncurses_erasechar) — Returns
    current erase character
-   [ncurses\_filter](/ref/ncurses.html#ncurses_filter) — Set LINES for
    iniscr() and newterm() to 1
-   [ncurses\_flash](/ref/ncurses.html#ncurses_flash) — Flash terminal
    screen (visual bell)
-   [ncurses\_flushinp](/ref/ncurses.html#ncurses_flushinp) — Flush
    keyboard input buffer
-   [ncurses\_getch](/ref/ncurses.html#ncurses_getch) — Read a character
    from keyboard
-   [ncurses\_getmaxyx](/ref/ncurses.html#ncurses_getmaxyx) — Returns
    the size of a window
-   [ncurses\_getmouse](/ref/ncurses.html#ncurses_getmouse) — Reads
    mouse event
-   [ncurses\_getyx](/ref/ncurses.html#ncurses_getyx) — Returns the
    current cursor position for a window
-   [ncurses\_halfdelay](/ref/ncurses.html#ncurses_halfdelay) — Put
    terminal into halfdelay mode
-   [ncurses\_has\_colors](/ref/ncurses.html#ncurses_has_colors) —
    Checks if terminal has color capabilities
-   [ncurses\_has\_ic](/ref/ncurses.html#ncurses_has_ic) — Check for
    insert- and delete-capabilities
-   [ncurses\_has\_il](/ref/ncurses.html#ncurses_has_il) — Check for
    line insert- and delete-capabilities
-   [ncurses\_has\_key](/ref/ncurses.html#ncurses_has_key) — Check for
    presence of a function key on terminal keyboard
-   [ncurses\_hide\_panel](/ref/ncurses.html#ncurses_hide_panel) —
    Remove panel from the stack, making it invisible
-   [ncurses\_hline](/ref/ncurses.html#ncurses_hline) — Draw a
    horizontal line at current position using an attributed character
    and max. n characters long
-   [ncurses\_inch](/ref/ncurses.html#ncurses_inch) — Get character and
    attribute at current position
-   [ncurses\_init\_color](/ref/ncurses.html#ncurses_init_color) —
    Define a terminal color
-   [ncurses\_init\_pair](/ref/ncurses.html#ncurses_init_pair) — Define
    a color pair
-   [ncurses\_init](/ref/ncurses.html#ncurses_init) — Initialize ncurses
-   [ncurses\_insch](/ref/ncurses.html#ncurses_insch) — Insert character
    moving rest of line including character at current position
-   [ncurses\_insdelln](/ref/ncurses.html#ncurses_insdelln) — Insert
    lines before current line scrolling down (negative numbers delete
    and scroll up)
-   [ncurses\_insertln](/ref/ncurses.html#ncurses_insertln) — Insert a
    line, move rest of screen down
-   [ncurses\_insstr](/ref/ncurses.html#ncurses_insstr) — Insert string
    at current position, moving rest of line right
-   [ncurses\_instr](/ref/ncurses.html#ncurses_instr) — Reads string
    from terminal screen
-   [ncurses\_isendwin](/ref/ncurses.html#ncurses_isendwin) — Ncurses is
    in endwin mode, normal screen output may be performed
-   [ncurses\_keyok](/ref/ncurses.html#ncurses_keyok) — Enable or
    disable a keycode
-   [ncurses\_keypad](/ref/ncurses.html#ncurses_keypad) — Turns keypad
    on or off
-   [ncurses\_killchar](/ref/ncurses.html#ncurses_killchar) — Returns
    current line kill character
-   [ncurses\_longname](/ref/ncurses.html#ncurses_longname) — Returns
    terminals description
-   [ncurses\_meta](/ref/ncurses.html#ncurses_meta) — Enables/Disable
    8-bit meta key information
-   [ncurses\_mouse\_trafo](/ref/ncurses.html#ncurses_mouse_trafo) —
    Transforms coordinates
-   [ncurses\_mouseinterval](/ref/ncurses.html#ncurses_mouseinterval) —
    Set timeout for mouse button clicks
-   [ncurses\_mousemask](/ref/ncurses.html#ncurses_mousemask) — Sets
    mouse options
-   [ncurses\_move\_panel](/ref/ncurses.html#ncurses_move_panel) — Moves
    a panel so that its upper-left corner is at \[startx, starty\]
-   [ncurses\_move](/ref/ncurses.html#ncurses_move) — Move output
    position
-   [ncurses\_mvaddch](/ref/ncurses.html#ncurses_mvaddch) — Move current
    position and add character
-   [ncurses\_mvaddchnstr](/ref/ncurses.html#ncurses_mvaddchnstr) — Move
    position and add attributed string with specified length
-   [ncurses\_mvaddchstr](/ref/ncurses.html#ncurses_mvaddchstr) — Move
    position and add attributed string
-   [ncurses\_mvaddnstr](/ref/ncurses.html#ncurses_mvaddnstr) — Move
    position and add string with specified length
-   [ncurses\_mvaddstr](/ref/ncurses.html#ncurses_mvaddstr) — Move
    position and add string
-   [ncurses\_mvcur](/ref/ncurses.html#ncurses_mvcur) — Move cursor
    immediately
-   [ncurses\_mvdelch](/ref/ncurses.html#ncurses_mvdelch) — Move
    position and delete character, shift rest of line left
-   [ncurses\_mvgetch](/ref/ncurses.html#ncurses_mvgetch) — Move
    position and get character at new position
-   [ncurses\_mvhline](/ref/ncurses.html#ncurses_mvhline) — Set new
    position and draw a horizontal line using an attributed character
    and max. n characters long
-   [ncurses\_mvinch](/ref/ncurses.html#ncurses_mvinch) — Move position
    and get attributed character at new position
-   [ncurses\_mvvline](/ref/ncurses.html#ncurses_mvvline) — Set new
    position and draw a vertical line using an attributed character and
    max. n characters long
-   [ncurses\_mvwaddstr](/ref/ncurses.html#ncurses_mvwaddstr) — Add
    string at new position in window
-   [ncurses\_napms](/ref/ncurses.html#ncurses_napms) — Sleep
-   [ncurses\_new\_panel](/ref/ncurses.html#ncurses_new_panel) — Create
    a new panel and associate it with window
-   [ncurses\_newpad](/ref/ncurses.html#ncurses_newpad) — Creates a new
    pad (window)
-   [ncurses\_newwin](/ref/ncurses.html#ncurses_newwin) — Create a new
    window
-   [ncurses\_nl](/ref/ncurses.html#ncurses_nl) — Translate newline and
    carriage return / line feed
-   [ncurses\_nocbreak](/ref/ncurses.html#ncurses_nocbreak) — Switch
    terminal to cooked mode
-   [ncurses\_noecho](/ref/ncurses.html#ncurses_noecho) — Switch off
    keyboard input echo
-   [ncurses\_nonl](/ref/ncurses.html#ncurses_nonl) — Do not translate
    newline and carriage return / line feed
-   [ncurses\_noqiflush](/ref/ncurses.html#ncurses_noqiflush) — Do not
    flush on signal characters
-   [ncurses\_noraw](/ref/ncurses.html#ncurses_noraw) — Switch terminal
    out of raw mode
-   [ncurses\_pair\_content](/ref/ncurses.html#ncurses_pair_content) —
    Retrieves foreground and background colors of a color pair
-   [ncurses\_panel\_above](/ref/ncurses.html#ncurses_panel_above) —
    Returns the panel above panel
-   [ncurses\_panel\_below](/ref/ncurses.html#ncurses_panel_below) —
    Returns the panel below panel
-   [ncurses\_panel\_window](/ref/ncurses.html#ncurses_panel_window) —
    Returns the window associated with panel
-   [ncurses\_pnoutrefresh](/ref/ncurses.html#ncurses_pnoutrefresh) —
    Copies a region from a pad into the virtual screen
-   [ncurses\_prefresh](/ref/ncurses.html#ncurses_prefresh) — Copies a
    region from a pad into the virtual screen
-   [ncurses\_putp](/ref/ncurses.html#ncurses_putp) — Apply padding
    information to the string and output it
-   [ncurses\_qiflush](/ref/ncurses.html#ncurses_qiflush) — Flush on
    signal characters
-   [ncurses\_raw](/ref/ncurses.html#ncurses_raw) — Switch terminal into
    raw mode
-   [ncurses\_refresh](/ref/ncurses.html#ncurses_refresh) — Refresh
    screen
-   [ncurses\_replace\_panel](/ref/ncurses.html#ncurses_replace_panel) —
    Replaces the window associated with panel
-   [ncurses\_reset\_prog\_mode](/ref/ncurses.html#ncurses_reset_prog_mode)
    — Resets the prog mode saved by def\_prog\_mode
-   [ncurses\_reset\_shell\_mode](/ref/ncurses.html#ncurses_reset_shell_mode)
    — Resets the shell mode saved by def\_shell\_mode
-   [ncurses\_resetty](/ref/ncurses.html#ncurses_resetty) — Restores
    saved terminal state
-   [ncurses\_savetty](/ref/ncurses.html#ncurses_savetty) — Saves
    terminal state
-   [ncurses\_scr\_dump](/ref/ncurses.html#ncurses_scr_dump) — Dump
    screen content to file
-   [ncurses\_scr\_init](/ref/ncurses.html#ncurses_scr_init) —
    Initialize screen from file dump
-   [ncurses\_scr\_restore](/ref/ncurses.html#ncurses_scr_restore) —
    Restore screen from file dump
-   [ncurses\_scr\_set](/ref/ncurses.html#ncurses_scr_set) — Inherit
    screen from file dump
-   [ncurses\_scrl](/ref/ncurses.html#ncurses_scrl) — Scroll window
    content up or down without changing current position
-   [ncurses\_show\_panel](/ref/ncurses.html#ncurses_show_panel) —
    Places an invisible panel on top of the stack, making it visible
-   [ncurses\_slk\_attr](/ref/ncurses.html#ncurses_slk_attr) — Returns
    current soft label key attribute
-   [ncurses\_slk\_attroff](/ref/ncurses.html#ncurses_slk_attroff) —
    Turn off the given attributes for soft function-key labels
-   [ncurses\_slk\_attron](/ref/ncurses.html#ncurses_slk_attron) — Turn
    on the given attributes for soft function-key labels
-   [ncurses\_slk\_attrset](/ref/ncurses.html#ncurses_slk_attrset) — Set
    given attributes for soft function-key labels
-   [ncurses\_slk\_clear](/ref/ncurses.html#ncurses_slk_clear) — Clears
    soft labels from screen
-   [ncurses\_slk\_color](/ref/ncurses.html#ncurses_slk_color) — Sets
    color for soft label keys
-   [ncurses\_slk\_init](/ref/ncurses.html#ncurses_slk_init) —
    Initializes soft label key functions
-   [ncurses\_slk\_noutrefresh](/ref/ncurses.html#ncurses_slk_noutrefresh)
    — Copies soft label keys to virtual screen
-   [ncurses\_slk\_refresh](/ref/ncurses.html#ncurses_slk_refresh) —
    Copies soft label keys to screen
-   [ncurses\_slk\_restore](/ref/ncurses.html#ncurses_slk_restore) —
    Restores soft label keys
-   [ncurses\_slk\_set](/ref/ncurses.html#ncurses_slk_set) — Sets
    function key labels
-   [ncurses\_slk\_touch](/ref/ncurses.html#ncurses_slk_touch) — Forces
    output when ncurses\_slk\_noutrefresh is performed
-   [ncurses\_standend](/ref/ncurses.html#ncurses_standend) — Stop using
    'standout' attribute
-   [ncurses\_standout](/ref/ncurses.html#ncurses_standout) — Start
    using 'standout' attribute
-   [ncurses\_start\_color](/ref/ncurses.html#ncurses_start_color) —
    Initializes color functionality
-   [ncurses\_termattrs](/ref/ncurses.html#ncurses_termattrs) — Returns
    a logical OR of all attribute flags supported by terminal
-   [ncurses\_termname](/ref/ncurses.html#ncurses_termname) — Returns
    terminals (short)-name
-   [ncurses\_timeout](/ref/ncurses.html#ncurses_timeout) — Set timeout
    for special key sequences
-   [ncurses\_top\_panel](/ref/ncurses.html#ncurses_top_panel) — Moves a
    visible panel to the top of the stack
-   [ncurses\_typeahead](/ref/ncurses.html#ncurses_typeahead) — Specify
    different filedescriptor for typeahead checking
-   [ncurses\_ungetch](/ref/ncurses.html#ncurses_ungetch) — Put a
    character back into the input stream
-   [ncurses\_ungetmouse](/ref/ncurses.html#ncurses_ungetmouse) — Pushes
    mouse event to queue
-   [ncurses\_update\_panels](/ref/ncurses.html#ncurses_update_panels) —
    Refreshes the virtual screen to reflect the relations between panels
    in the stack
-   [ncurses\_use\_default\_colors](/ref/ncurses.html#ncurses_use_default_colors)
    — Assign terminal default colors to color id -1
-   [ncurses\_use\_env](/ref/ncurses.html#ncurses_use_env) — Control use
    of environment information about terminal size
-   [ncurses\_use\_extended\_names](/ref/ncurses.html#ncurses_use_extended_names)
    — Control use of extended names in terminfo descriptions
-   [ncurses\_vidattr](/ref/ncurses.html#ncurses_vidattr) — Display the
    string on the terminal in the video attribute mode
-   [ncurses\_vline](/ref/ncurses.html#ncurses_vline) — Draw a vertical
    line at current position using an attributed character and max. n
    characters long
-   [ncurses\_waddch](/ref/ncurses.html#ncurses_waddch) — Adds character
    at current position in a window and advance cursor
-   [ncurses\_waddstr](/ref/ncurses.html#ncurses_waddstr) — Outputs text
    at current postion in window
-   [ncurses\_wattroff](/ref/ncurses.html#ncurses_wattroff) — Turns off
    attributes for a window
-   [ncurses\_wattron](/ref/ncurses.html#ncurses_wattron) — Turns on
    attributes for a window
-   [ncurses\_wattrset](/ref/ncurses.html#ncurses_wattrset) — Set the
    attributes for a window
-   [ncurses\_wborder](/ref/ncurses.html#ncurses_wborder) — Draws a
    border around the window using attributed characters
-   [ncurses\_wclear](/ref/ncurses.html#ncurses_wclear) — Clears window
-   [ncurses\_wcolor\_set](/ref/ncurses.html#ncurses_wcolor_set) — Sets
    windows color pairings
-   [ncurses\_werase](/ref/ncurses.html#ncurses_werase) — Erase window
    contents
-   [ncurses\_wgetch](/ref/ncurses.html#ncurses_wgetch) — Reads a
    character from keyboard (window)
-   [ncurses\_whline](/ref/ncurses.html#ncurses_whline) — Draws a
    horizontal line in a window at current position using an attributed
    character and max. n characters long
-   [ncurses\_wmouse\_trafo](/ref/ncurses.html#ncurses_wmouse_trafo) —
    Transforms window/stdscr coordinates
-   [ncurses\_wmove](/ref/ncurses.html#ncurses_wmove) — Moves windows
    output position
-   [ncurses\_wnoutrefresh](/ref/ncurses.html#ncurses_wnoutrefresh) —
    Copies window to virtual screen
-   [ncurses\_wrefresh](/ref/ncurses.html#ncurses_wrefresh) — Refresh
    window on terminal screen
-   [ncurses\_wstandend](/ref/ncurses.html#ncurses_wstandend) — End
    standout mode for a window
-   [ncurses\_wstandout](/ref/ncurses.html#ncurses_wstandout) — Enter
    standout mode for a window
-   [ncurses\_wvline](/ref/ncurses.html#ncurses_wvline) — Draws a
    vertical line in a window at current position using an attributed
    character and max. n characters long
