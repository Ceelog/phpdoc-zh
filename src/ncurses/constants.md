预定义常量
==========

**目录**

-   [Error codes](/ncurses/constants.html#Error%20codes)
-   [Colors](/ncurses/constants.html#Colors)
-   [Keys](/ncurses/constants.html#Keys)
-   [Mouse](/ncurses/constants.html#Mouse)

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

Error codes
-----------

On error ncurses functions return *-1*. Some functions return *0* on
success. See the relevant pages in the documentation for actual return
values.

Colors
------

| constant                    | meaning                                            |
|-----------------------------|----------------------------------------------------|
| **`NCURSES_COLOR_BLACK`**   | no color (black)                                   |
| **`NCURSES_COLOR_WHITE`**   | white                                              |
| **`NCURSES_COLOR_RED`**     | red - supported when terminal is in color mode     |
| **`NCURSES_COLOR_GREEN`**   | green - supported when terminal is in color mode   |
| **`NCURSES_COLOR_YELLOW`**  | yellow - supported when terminal is in color mode  |
| **`NCURSES_COLOR_BLUE`**    | blue - supported when terminal is in color mode    |
| **`NCURSES_COLOR_CYAN`**    | cyan - supported when terminal is in color mode    |
| **`NCURSES_COLOR_MAGENTA`** | magenta - supported when terminal is in color mode |

Keys
----

| constant                                     | meaning                          |
|----------------------------------------------|----------------------------------|
| **`NCURSES_KEY_F0`** - **`NCURSES_KEY_F64`** | function keys F1 - F64           |
| **`NCURSES_KEY_DOWN`**                       | down arrow                       |
| **`NCURSES_KEY_UP`**                         | up arrow                         |
| **`NCURSES_KEY_LEFT`**                       | left arrow                       |
| **`NCURSES_KEY_RIGHT`**                      | right arrow                      |
| **`NCURSES_KEY_HOME`**                       | home key (upward+left arrow)     |
| **`NCURSES_KEY_BACKSPACE`**                  | backspace                        |
| **`NCURSES_KEY_DL`**                         | delete line                      |
| **`NCURSES_KEY_IL`**                         | insert line                      |
| **`NCURSES_KEY_DC`**                         | delete character                 |
| **`NCURSES_KEY_IC`**                         | insert char or enter insert mode |
| **`NCURSES_KEY_EIC`**                        | exit insert char mode            |
| **`NCURSES_KEY_CLEAR`**                      | clear screen                     |
| **`NCURSES_KEY_EOS`**                        | clear to end of screen           |
| **`NCURSES_KEY_EOL`**                        | clear to end of line             |
| **`NCURSES_KEY_SF`**                         | scroll one line forward          |
| **`NCURSES_KEY_SR`**                         | scroll one line backward         |
| **`NCURSES_KEY_NPAGE`**                      | next page                        |
| **`NCURSES_KEY_PPAGE`**                      | previous page                    |
| **`NCURSES_KEY_STAB`**                       | set tab                          |
| **`NCURSES_KEY_CTAB`**                       | clear tab                        |
| **`NCURSES_KEY_CATAB`**                      | clear all tabs                   |
| **`NCURSES_KEY_SRESET`**                     | soft (partial) reset             |
| **`NCURSES_KEY_RESET`**                      | reset or hard reset              |
| **`NCURSES_KEY_PRINT`**                      | print                            |
| **`NCURSES_KEY_LL`**                         | lower left                       |
| **`NCURSES_KEY_A1`**                         | upper left of keypad             |
| **`NCURSES_KEY_A3`**                         | upper right of keypad            |
| **`NCURSES_KEY_B2`**                         | center of keypad                 |
| **`NCURSES_KEY_C1`**                         | lower left of keypad             |
| **`NCURSES_KEY_C3`**                         | lower right of keypad            |
| **`NCURSES_KEY_BTAB`**                       | back tab                         |
| **`NCURSES_KEY_BEG`**                        | beginning                        |
| **`NCURSES_KEY_CANCEL`**                     | cancel                           |
| **`NCURSES_KEY_CLOSE`**                      | close                            |
| **`NCURSES_KEY_COMMAND`**                    | cmd (command)                    |
| **`NCURSES_KEY_COPY`**                       | copy                             |
| **`NCURSES_KEY_CREATE`**                     | create                           |
| **`NCURSES_KEY_END`**                        | end                              |
| **`NCURSES_KEY_EXIT`**                       | exit                             |
| **`NCURSES_KEY_FIND`**                       | find                             |
| **`NCURSES_KEY_HELP`**                       | help                             |
| **`NCURSES_KEY_MARK`**                       | mark                             |
| **`NCURSES_KEY_MESSAGE`**                    | message                          |
| **`NCURSES_KEY_MOVE`**                       | move                             |
| **`NCURSES_KEY_NEXT`**                       | next                             |
| **`NCURSES_KEY_OPEN`**                       | open                             |
| **`NCURSES_KEY_OPTIONS`**                    | options                          |
| **`NCURSES_KEY_PREVIOUS`**                   | previous                         |
| **`NCURSES_KEY_REDO`**                       | redo                             |
| **`NCURSES_KEY_REFERENCE`**                  | ref (reference)                  |
| **`NCURSES_KEY_REFRESH`**                    | refresh                          |
| **`NCURSES_KEY_REPLACE`**                    | replace                          |
| **`NCURSES_KEY_RESTART`**                    | restart                          |
| **`NCURSES_KEY_RESUME`**                     | resume                           |
| **`NCURSES_KEY_SAVE`**                       | save                             |
| **`NCURSES_KEY_SBEG`**                       | shiftet beg (beginning)          |
| **`NCURSES_KEY_SCANCEL`**                    | shifted cancel                   |
| **`NCURSES_KEY_SCOMMAND`**                   | shifted command                  |
| **`NCURSES_KEY_SCOPY`**                      | shifted copy                     |
| **`NCURSES_KEY_SCREATE`**                    | shifted create                   |
| **`NCURSES_KEY_SDC`**                        | shifted delete char              |
| **`NCURSES_KEY_SDL`**                        | shifted delete line              |
| **`NCURSES_KEY_SELECT`**                     | select                           |
| **`NCURSES_KEY_SEND`**                       | shifted end                      |
| **`NCURSES_KEY_SEOL`**                       | shifted end of line              |
| **`NCURSES_KEY_SEXIT`**                      | shifted exit                     |
| **`NCURSES_KEY_SFIND`**                      | shifted find                     |
| **`NCURSES_KEY_SHELP`**                      | shifted help                     |
| **`NCURSES_KEY_SHOME`**                      | shifted home                     |
| **`NCURSES_KEY_SIC`**                        | shifted input                    |
| **`NCURSES_KEY_SLEFT`**                      | shifted left arrow               |
| **`NCURSES_KEY_SMESSAGE`**                   | shifted message                  |
| **`NCURSES_KEY_SMOVE`**                      | shifted move                     |
| **`NCURSES_KEY_SNEXT`**                      | shifted next                     |
| **`NCURSES_KEY_SOPTIONS`**                   | shifted options                  |
| **`NCURSES_KEY_SPREVIOUS`**                  | shifted previous                 |
| **`NCURSES_KEY_SPRINT`**                     | shifted print                    |
| **`NCURSES_KEY_SREDO`**                      | shifted redo                     |
| **`NCURSES_KEY_SREPLACE`**                   | shifted replace                  |
| **`NCURSES_KEY_SRIGHT`**                     | shifted right arrow              |
| **`NCURSES_KEY_SRSUME`**                     | shifted resume                   |
| **`NCURSES_KEY_SSAVE`**                      | shifted save                     |
| **`NCURSES_KEY_SSUSPEND`**                   | shifted suspend                  |
| **`NCURSES_KEY_UNDO`**                       | undo                             |
| **`NCURSES_KEY_MOUSE`**                      | mouse event has occurred         |
| **`NCURSES_KEY_MAX`**                        | maximum key value                |

Mouse
-----

| Constant                                                                    | meaning                     |
|-----------------------------------------------------------------------------|-----------------------------|
| **`NCURSES_BUTTON1_RELEASED`** - **`NCURSES_BUTTON4_RELEASED`**             | button (1-4) released       |
| **`NCURSES_BUTTON1_PRESSED`** - **`NCURSES_BUTTON4_PRESSED`**               | button (1-4) pressed        |
| **`NCURSES_BUTTON1_CLICKED`** - **`NCURSES_BUTTON4_CLICKED`**               | button (1-4) clicked        |
| **`NCURSES_BUTTON1_DOUBLE_CLICKED`** - **`NCURSES_BUTTON4_DOUBLE_CLICKED`** | button (1-4) double clicked |
| **`NCURSES_BUTTON1_TRIPLE_CLICKED`** - **`NCURSES_BUTTON4_TRIPLE_CLICKED`** | button (1-4) triple clicked |
| **`NCURSES_BUTTON_CTRL`**                                                   | ctrl pressed during click   |
| **`NCURSES_BUTTON_SHIFT`**                                                  | shift pressed during click  |
| **`NCURSES_BUTTON_ALT`**                                                    | alt pressed during click    |
| **`NCURSES_ALL_MOUSE_EVENTS`**                                              | report all mouse events     |
| **`NCURSES_REPORT_MOUSE_POSITION`**                                         | report mouse position       |
