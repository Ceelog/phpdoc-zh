Ncurses Terminal Screen Control
===============================

**目录**

-   [简介](/intro/ncurses.html)
-   [安装／配置](/ncurses/setup.html)
    -   [需求](/ncurses/setup.html#需求)
    -   [安装](/ncurses/setup.html#安装)
    -   [运行时配置](/ncurses/setup.html#运行时配置)
    -   [资源类型](/ncurses/setup.html#资源类型)
-   [预定义常量](/ncurses/constants.html)
    -   [Error codes](/ncurses/constants.html#Error%20codes)
    -   [Colors](/ncurses/constants.html#Colors)
    -   [Keys](/ncurses/constants.html#Keys)
    -   [Mouse](/ncurses/constants.html#Mouse)
-   [Ncurses 函数](/ref/ncurses.html)
    -   [ncurses\_addch](/ref/ncurses.html#ncurses_addch) — Add
        character at current position and advance cursor
    -   [ncurses\_addchnstr](/ref/ncurses.html#ncurses_addchnstr) — Add
        attributed string with specified length at current position
    -   [ncurses\_addchstr](/ref/ncurses.html#ncurses_addchstr) — Add
        attributed string at current position
    -   [ncurses\_addnstr](/ref/ncurses.html#ncurses_addnstr) — Add
        string with specified length at current position
    -   [ncurses\_addstr](/ref/ncurses.html#ncurses_addstr) — Output
        text at current position
    -   [ncurses\_assume\_default\_colors](/ref/ncurses.html#ncurses_assume_default_colors)
        — Define default colors for color 0
    -   [ncurses\_attroff](/ref/ncurses.html#ncurses_attroff) — Turn off
        the given attributes
    -   [ncurses\_attron](/ref/ncurses.html#ncurses_attron) — Turn on
        the given attributes
    -   [ncurses\_attrset](/ref/ncurses.html#ncurses_attrset) — Set
        given attributes
    -   [ncurses\_baudrate](/ref/ncurses.html#ncurses_baudrate) —
        Returns baudrate of terminal
    -   [ncurses\_beep](/ref/ncurses.html#ncurses_beep) — Let the
        terminal beep
    -   [ncurses\_bkgd](/ref/ncurses.html#ncurses_bkgd) — Set background
        property for terminal screen
    -   [ncurses\_bkgdset](/ref/ncurses.html#ncurses_bkgdset) — Control
        screen background
    -   [ncurses\_border](/ref/ncurses.html#ncurses_border) — Draw a
        border around the screen using attributed characters
    -   [ncurses\_bottom\_panel](/ref/ncurses.html#ncurses_bottom_panel)
        — Moves a visible panel to the bottom of the stack
    -   [ncurses\_can\_change\_color](/ref/ncurses.html#ncurses_can_change_color)
        — Checks if terminal color definitions can be changed
    -   [ncurses\_cbreak](/ref/ncurses.html#ncurses_cbreak) — Switch off
        input buffering
    -   [ncurses\_clear](/ref/ncurses.html#ncurses_clear) — Clear screen
    -   [ncurses\_clrtobot](/ref/ncurses.html#ncurses_clrtobot) — Clear
        screen from current position to bottom
    -   [ncurses\_clrtoeol](/ref/ncurses.html#ncurses_clrtoeol) — Clear
        screen from current position to end of line
    -   [ncurses\_color\_content](/ref/ncurses.html#ncurses_color_content)
        — Retrieves RGB components of a color
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
    -   [ncurses\_del\_panel](/ref/ncurses.html#ncurses_del_panel) —
        Remove panel from the stack and delete it (but not the
        associated window)
    -   [ncurses\_delay\_output](/ref/ncurses.html#ncurses_delay_output)
        — Delay output on terminal using padding characters
    -   [ncurses\_delch](/ref/ncurses.html#ncurses_delch) — Delete
        character at current position, move rest of line left
    -   [ncurses\_deleteln](/ref/ncurses.html#ncurses_deleteln) — Delete
        line at current position, move rest of screen up
    -   [ncurses\_delwin](/ref/ncurses.html#ncurses_delwin) — Delete a
        ncurses window
    -   [ncurses\_doupdate](/ref/ncurses.html#ncurses_doupdate) — Write
        all prepared refreshes to terminal
    -   [ncurses\_echo](/ref/ncurses.html#ncurses_echo) — Activate
        keyboard input echo
    -   [ncurses\_echochar](/ref/ncurses.html#ncurses_echochar) — Single
        character output including refresh
    -   [ncurses\_end](/ref/ncurses.html#ncurses_end) — Stop using
        ncurses, clean up the screen
    -   [ncurses\_erase](/ref/ncurses.html#ncurses_erase) — Erase
        terminal screen
    -   [ncurses\_erasechar](/ref/ncurses.html#ncurses_erasechar) —
        Returns current erase character
    -   [ncurses\_filter](/ref/ncurses.html#ncurses_filter) — Set LINES
        for iniscr() and newterm() to 1
    -   [ncurses\_flash](/ref/ncurses.html#ncurses_flash) — Flash
        terminal screen (visual bell)
    -   [ncurses\_flushinp](/ref/ncurses.html#ncurses_flushinp) — Flush
        keyboard input buffer
    -   [ncurses\_getch](/ref/ncurses.html#ncurses_getch) — Read a
        character from keyboard
    -   [ncurses\_getmaxyx](/ref/ncurses.html#ncurses_getmaxyx) —
        Returns the size of a window
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
    -   [ncurses\_has\_key](/ref/ncurses.html#ncurses_has_key) — Check
        for presence of a function key on terminal keyboard
    -   [ncurses\_hide\_panel](/ref/ncurses.html#ncurses_hide_panel) —
        Remove panel from the stack, making it invisible
    -   [ncurses\_hline](/ref/ncurses.html#ncurses_hline) — Draw a
        horizontal line at current position using an attributed
        character and max. n characters long
    -   [ncurses\_inch](/ref/ncurses.html#ncurses_inch) — Get character
        and attribute at current position
    -   [ncurses\_init\_color](/ref/ncurses.html#ncurses_init_color) —
        Define a terminal color
    -   [ncurses\_init\_pair](/ref/ncurses.html#ncurses_init_pair) —
        Define a color pair
    -   [ncurses\_init](/ref/ncurses.html#ncurses_init) — Initialize
        ncurses
    -   [ncurses\_insch](/ref/ncurses.html#ncurses_insch) — Insert
        character moving rest of line including character at current
        position
    -   [ncurses\_insdelln](/ref/ncurses.html#ncurses_insdelln) — Insert
        lines before current line scrolling down (negative numbers
        delete and scroll up)
    -   [ncurses\_insertln](/ref/ncurses.html#ncurses_insertln) — Insert
        a line, move rest of screen down
    -   [ncurses\_insstr](/ref/ncurses.html#ncurses_insstr) — Insert
        string at current position, moving rest of line right
    -   [ncurses\_instr](/ref/ncurses.html#ncurses_instr) — Reads string
        from terminal screen
    -   [ncurses\_isendwin](/ref/ncurses.html#ncurses_isendwin) —
        Ncurses is in endwin mode, normal screen output may be performed
    -   [ncurses\_keyok](/ref/ncurses.html#ncurses_keyok) — Enable or
        disable a keycode
    -   [ncurses\_keypad](/ref/ncurses.html#ncurses_keypad) — Turns
        keypad on or off
    -   [ncurses\_killchar](/ref/ncurses.html#ncurses_killchar) —
        Returns current line kill character
    -   [ncurses\_longname](/ref/ncurses.html#ncurses_longname) —
        Returns terminals description
    -   [ncurses\_meta](/ref/ncurses.html#ncurses_meta) —
        Enables/Disable 8-bit meta key information
    -   [ncurses\_mouse\_trafo](/ref/ncurses.html#ncurses_mouse_trafo) —
        Transforms coordinates
    -   [ncurses\_mouseinterval](/ref/ncurses.html#ncurses_mouseinterval)
        — Set timeout for mouse button clicks
    -   [ncurses\_mousemask](/ref/ncurses.html#ncurses_mousemask) — Sets
        mouse options
    -   [ncurses\_move\_panel](/ref/ncurses.html#ncurses_move_panel) —
        Moves a panel so that its upper-left corner is at \[startx,
        starty\]
    -   [ncurses\_move](/ref/ncurses.html#ncurses_move) — Move output
        position
    -   [ncurses\_mvaddch](/ref/ncurses.html#ncurses_mvaddch) — Move
        current position and add character
    -   [ncurses\_mvaddchnstr](/ref/ncurses.html#ncurses_mvaddchnstr) —
        Move position and add attributed string with specified length
    -   [ncurses\_mvaddchstr](/ref/ncurses.html#ncurses_mvaddchstr) —
        Move position and add attributed string
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
        position and draw a horizontal line using an attributed
        character and max. n characters long
    -   [ncurses\_mvinch](/ref/ncurses.html#ncurses_mvinch) — Move
        position and get attributed character at new position
    -   [ncurses\_mvvline](/ref/ncurses.html#ncurses_mvvline) — Set new
        position and draw a vertical line using an attributed character
        and max. n characters long
    -   [ncurses\_mvwaddstr](/ref/ncurses.html#ncurses_mvwaddstr) — Add
        string at new position in window
    -   [ncurses\_napms](/ref/ncurses.html#ncurses_napms) — Sleep
    -   [ncurses\_new\_panel](/ref/ncurses.html#ncurses_new_panel) —
        Create a new panel and associate it with window
    -   [ncurses\_newpad](/ref/ncurses.html#ncurses_newpad) — Creates a
        new pad (window)
    -   [ncurses\_newwin](/ref/ncurses.html#ncurses_newwin) — Create a
        new window
    -   [ncurses\_nl](/ref/ncurses.html#ncurses_nl) — Translate newline
        and carriage return / line feed
    -   [ncurses\_nocbreak](/ref/ncurses.html#ncurses_nocbreak) — Switch
        terminal to cooked mode
    -   [ncurses\_noecho](/ref/ncurses.html#ncurses_noecho) — Switch off
        keyboard input echo
    -   [ncurses\_nonl](/ref/ncurses.html#ncurses_nonl) — Do not
        translate newline and carriage return / line feed
    -   [ncurses\_noqiflush](/ref/ncurses.html#ncurses_noqiflush) — Do
        not flush on signal characters
    -   [ncurses\_noraw](/ref/ncurses.html#ncurses_noraw) — Switch
        terminal out of raw mode
    -   [ncurses\_pair\_content](/ref/ncurses.html#ncurses_pair_content)
        — Retrieves foreground and background colors of a color pair
    -   [ncurses\_panel\_above](/ref/ncurses.html#ncurses_panel_above) —
        Returns the panel above panel
    -   [ncurses\_panel\_below](/ref/ncurses.html#ncurses_panel_below) —
        Returns the panel below panel
    -   [ncurses\_panel\_window](/ref/ncurses.html#ncurses_panel_window)
        — Returns the window associated with panel
    -   [ncurses\_pnoutrefresh](/ref/ncurses.html#ncurses_pnoutrefresh)
        — Copies a region from a pad into the virtual screen
    -   [ncurses\_prefresh](/ref/ncurses.html#ncurses_prefresh) — Copies
        a region from a pad into the virtual screen
    -   [ncurses\_putp](/ref/ncurses.html#ncurses_putp) — Apply padding
        information to the string and output it
    -   [ncurses\_qiflush](/ref/ncurses.html#ncurses_qiflush) — Flush on
        signal characters
    -   [ncurses\_raw](/ref/ncurses.html#ncurses_raw) — Switch terminal
        into raw mode
    -   [ncurses\_refresh](/ref/ncurses.html#ncurses_refresh) — Refresh
        screen
    -   [ncurses\_replace\_panel](/ref/ncurses.html#ncurses_replace_panel)
        — Replaces the window associated with panel
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
    -   [ncurses\_slk\_attr](/ref/ncurses.html#ncurses_slk_attr) —
        Returns current soft label key attribute
    -   [ncurses\_slk\_attroff](/ref/ncurses.html#ncurses_slk_attroff) —
        Turn off the given attributes for soft function-key labels
    -   [ncurses\_slk\_attron](/ref/ncurses.html#ncurses_slk_attron) —
        Turn on the given attributes for soft function-key labels
    -   [ncurses\_slk\_attrset](/ref/ncurses.html#ncurses_slk_attrset) —
        Set given attributes for soft function-key labels
    -   [ncurses\_slk\_clear](/ref/ncurses.html#ncurses_slk_clear) —
        Clears soft labels from screen
    -   [ncurses\_slk\_color](/ref/ncurses.html#ncurses_slk_color) —
        Sets color for soft label keys
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
    -   [ncurses\_slk\_touch](/ref/ncurses.html#ncurses_slk_touch) —
        Forces output when ncurses\_slk\_noutrefresh is performed
    -   [ncurses\_standend](/ref/ncurses.html#ncurses_standend) — Stop
        using 'standout' attribute
    -   [ncurses\_standout](/ref/ncurses.html#ncurses_standout) — Start
        using 'standout' attribute
    -   [ncurses\_start\_color](/ref/ncurses.html#ncurses_start_color) —
        Initializes color functionality
    -   [ncurses\_termattrs](/ref/ncurses.html#ncurses_termattrs) —
        Returns a logical OR of all attribute flags supported by
        terminal
    -   [ncurses\_termname](/ref/ncurses.html#ncurses_termname) —
        Returns terminals (short)-name
    -   [ncurses\_timeout](/ref/ncurses.html#ncurses_timeout) — Set
        timeout for special key sequences
    -   [ncurses\_top\_panel](/ref/ncurses.html#ncurses_top_panel) —
        Moves a visible panel to the top of the stack
    -   [ncurses\_typeahead](/ref/ncurses.html#ncurses_typeahead) —
        Specify different filedescriptor for typeahead checking
    -   [ncurses\_ungetch](/ref/ncurses.html#ncurses_ungetch) — Put a
        character back into the input stream
    -   [ncurses\_ungetmouse](/ref/ncurses.html#ncurses_ungetmouse) —
        Pushes mouse event to queue
    -   [ncurses\_update\_panels](/ref/ncurses.html#ncurses_update_panels)
        — Refreshes the virtual screen to reflect the relations between
        panels in the stack
    -   [ncurses\_use\_default\_colors](/ref/ncurses.html#ncurses_use_default_colors)
        — Assign terminal default colors to color id -1
    -   [ncurses\_use\_env](/ref/ncurses.html#ncurses_use_env) — Control
        use of environment information about terminal size
    -   [ncurses\_use\_extended\_names](/ref/ncurses.html#ncurses_use_extended_names)
        — Control use of extended names in terminfo descriptions
    -   [ncurses\_vidattr](/ref/ncurses.html#ncurses_vidattr) — Display
        the string on the terminal in the video attribute mode
    -   [ncurses\_vline](/ref/ncurses.html#ncurses_vline) — Draw a
        vertical line at current position using an attributed character
        and max. n characters long
    -   [ncurses\_waddch](/ref/ncurses.html#ncurses_waddch) — Adds
        character at current position in a window and advance cursor
    -   [ncurses\_waddstr](/ref/ncurses.html#ncurses_waddstr) — Outputs
        text at current postion in window
    -   [ncurses\_wattroff](/ref/ncurses.html#ncurses_wattroff) — Turns
        off attributes for a window
    -   [ncurses\_wattron](/ref/ncurses.html#ncurses_wattron) — Turns on
        attributes for a window
    -   [ncurses\_wattrset](/ref/ncurses.html#ncurses_wattrset) — Set
        the attributes for a window
    -   [ncurses\_wborder](/ref/ncurses.html#ncurses_wborder) — Draws a
        border around the window using attributed characters
    -   [ncurses\_wclear](/ref/ncurses.html#ncurses_wclear) — Clears
        window
    -   [ncurses\_wcolor\_set](/ref/ncurses.html#ncurses_wcolor_set) —
        Sets windows color pairings
    -   [ncurses\_werase](/ref/ncurses.html#ncurses_werase) — Erase
        window contents
    -   [ncurses\_wgetch](/ref/ncurses.html#ncurses_wgetch) — Reads a
        character from keyboard (window)
    -   [ncurses\_whline](/ref/ncurses.html#ncurses_whline) — Draws a
        horizontal line in a window at current position using an
        attributed character and max. n characters long
    -   [ncurses\_wmouse\_trafo](/ref/ncurses.html#ncurses_wmouse_trafo)
        — Transforms window/stdscr coordinates
    -   [ncurses\_wmove](/ref/ncurses.html#ncurses_wmove) — Moves
        windows output position
    -   [ncurses\_wnoutrefresh](/ref/ncurses.html#ncurses_wnoutrefresh)
        — Copies window to virtual screen
    -   [ncurses\_wrefresh](/ref/ncurses.html#ncurses_wrefresh) —
        Refresh window on terminal screen
    -   [ncurses\_wstandend](/ref/ncurses.html#ncurses_wstandend) — End
        standout mode for a window
    -   [ncurses\_wstandout](/ref/ncurses.html#ncurses_wstandout) —
        Enter standout mode for a window
    -   [ncurses\_wvline](/ref/ncurses.html#ncurses_wvline) — Draws a
        vertical line in a window at current position using an
        attributed character and max. n characters long
