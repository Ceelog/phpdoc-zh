预定义常量
==========

**目录**

-   [Newt form exit
    reasons](/newt/constants.html#Newt%20form%20exit%20reasons)
-   [Newt colorsets](/newt/constants.html#Newt%20colorsets)
-   [Newt argument flags](/newt/constants.html#Newt%20argument%20flags)
-   [Newt Flags Sense](/newt/constants.html#Newt%20Flags%20Sense)
-   [Newt Components
    Flags](/newt/constants.html#Newt%20Components%20Flags)
-   [File Descriptor
    Flags](/newt/constants.html#File%20Descriptor%20Flags)
-   [Checkbox Tree Flags](/newt/constants.html#Checkbox%20Tree%20Flags)
-   [Entry Flags](/newt/constants.html#Entry%20Flags)
-   [Listbox Flags](/newt/constants.html#Listbox%20Flags)
-   [Textbox Flags](/newt/constants.html#Textbox%20Flags)
-   [Form Flags](/newt/constants.html#Form%20Flags)
-   [Newt Keys](/newt/constants.html#Newt%20Keys)
-   [Newt Anchors](/newt/constants.html#Newt%20Anchors)
-   [Grid Flags](/newt/constants.html#Grid%20Flags)

下列常量由此扩展定义，且仅在此扩展编译入 PHP 或在运行时动态载入时可用。

Newt form exit reasons
----------------------

| constant                  | meaning                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| **`NEWT_EXIT_HOTKEY`**    | hotkey defined by <span class="function">newt\_form\_add\_hot\_key</span> was pressed                              |
| **`NEWT_EXIT_COMPONENT`** | some component has caused form to exit                                                                             |
| **`NEWT_EXIT_FDREADY`**   | file descriptor specified in <span class="function">newt\_form\_watch\_fd</span> is ready to be read or written to |
| **`NEWT_EXIT_TIMER`**     | time specified in <span class="function">newt\_form\_set\_timer</span> has elapsed                                 |

Newt colorsets
--------------

| constant                          | meaning |
|-----------------------------------|---------|
| **`NEWT_COLORSET_ROOT`**          |         |
| **`NEWT_COLORSET_BORDER`**        |         |
| **`NEWT_COLORSET_WINDOW`**        |         |
| **`NEWT_COLORSET_SHADOW`**        |         |
| **`NEWT_COLORSET_TITLE`**         |         |
| **`NEWT_COLORSET_BUTTON`**        |         |
| **`NEWT_COLORSET_ACTBUTTON`**     |         |
| **`NEWT_COLORSET_CHECKBOX`**      |         |
| **`NEWT_COLORSET_ACTCHECKBOX`**   |         |
| **`NEWT_COLORSET_ENTRY`**         |         |
| **`NEWT_COLORSET_LABEL`**         |         |
| **`NEWT_COLORSET_LISTBOX`**       |         |
| **`NEWT_COLORSET_ACTLISTBOX`**    |         |
| **`NEWT_COLORSET_TEXTBOX`**       |         |
| **`NEWT_COLORSET_ACTTEXTBOX`**    |         |
| **`NEWT_COLORSET_HELPLINE`**      |         |
| **`NEWT_COLORSET_ROOTTEXT`**      |         |
| **`NEWT_COLORSET_EMPTYSCALE`**    |         |
| **`NEWT_COLORSET_FULLSCALE`**     |         |
| **`NEWT_COLORSET_DISENTRY`**      |         |
| **`NEWT_COLORSET_COMPACTBUTTON`** |         |
| **`NEWT_COLORSET_ACTSELLISTBOX`** |         |
| **`NEWT_COLORSET_SELLISTBOX`**    |         |

Newt argument flags
-------------------

| constant              | meaning |
|-----------------------|---------|
| **`NEWT_ARG_LAST`**   |         |
| **`NEWT_ARG_APPEND`** |         |

Newt Flags Sense
----------------

| constant                | meaning |
|-------------------------|---------|
| **`NEWT_FLAGS_SET`**    |         |
| **`NEWT_FLAGS_RESET`**  |         |
| **`NEWT_FLAGS_TOGGLE`** |         |

Newt Components Flags
---------------------

| constant                   | meaning                                |
|----------------------------|----------------------------------------|
| **`NEWT_FLAG_RETURNEXIT`** | Exit form, when component is activated |
| **`NEWT_FLAG_HIDDEN`**     | Component is hidden                    |
| **`NEWT_FLAG_SCROLL`**     | Component is scrollable                |
| **`NEWT_FLAG_DISABLED`**   | Component is disabled                  |
| **`NEWT_FLAG_BORDER`**     |                                        |
| **`NEWT_FLAG_WRAP`**       | Wrap text                              |
| **`NEWT_FLAG_NOF12`**      | Don't exit form on pressing F12        |
| **`NEWT_FLAG_MULTIPLE`**   |                                        |
| **`NEWT_FLAG_SELECTED`**   | Component is selected                  |
| **`NEWT_FLAG_CHECKBOX`**   | Component is checkbox                  |
| **`NEWT_FLAG_PASSWORD`**   | Entry component is password entry      |
| **`NEWT_FLAG_SHOWCURSOR`** | Show cursor                            |

File Descriptor Flags
---------------------

| constant             | meaning |
|----------------------|---------|
| **`NEWT_FD_READ`**   |         |
| **`NEWT_FD_WRITE`**  |         |
| **`NEWT_FD_EXCEPT`** |         |

Checkbox Tree Flags
-------------------

| constant                             | meaning |
|--------------------------------------|---------|
| **`NEWT_CHECKBOXTREE_UNSELECTABLE`** |         |
| **`NEWT_CHECKBOXTREE_HIDE_BOX`**     |         |
| **`NEWT_CHECKBOXTREE_COLLAPSED`**    |         |
| **`NEWT_CHECKBOXTREE_EXPANDED`**     |         |
| **`NEWT_CHECKBOXTREE_UNSELECTED`**   |         |
| **`NEWT_CHECKBOXTREE_SELECTED`**     |         |

Entry Flags
-----------

| constant                    | meaning |
|-----------------------------|---------|
| **`NEWT_ENTRY_SCROLL`**     |         |
| **`NEWT_ENTRY_HIDDEN`**     |         |
| **`NEWT_ENTRY_RETURNEXIT`** |         |
| **`NEWT_ENTRY_DISABLED`**   |         |

Listbox Flags
-------------

| constant                      | meaning |
|-------------------------------|---------|
| **`NEWT_LISTBOX_RETURNEXIT`** |         |

Textbox Flags
-------------

| constant                  | meaning                    |
|---------------------------|----------------------------|
| **`NEWT_TEXTBOX_WRAP`**   | Wrap text in the textbox   |
| **`NEWT_TEXTBOX_SCROLL`** | Scroll text in the textbox |

Form Flags
----------

| constant              | meaning                      |
|-----------------------|------------------------------|
| **`NEWT_FORM_NOF12`** | Don't exit form on F12 press |

Newt Keys
---------

| constant                  | meaning |
|---------------------------|---------|
| **`NEWT_KEY_TAB`**        |         |
| **`NEWT_KEY_ENTER`**      |         |
| **`NEWT_KEY_SUSPEND`**    |         |
| **`NEWT_KEY_ESCAPE`**     |         |
| **`NEWT_KEY_RETURN`**     |         |
| **`NEWT_KEY_EXTRA_BASE`** |         |
| **`NEWT_KEY_UP`**         |         |
| **`NEWT_KEY_DOWN`**       |         |
| **`NEWT_KEY_LEFT`**       |         |
| **`NEWT_KEY_RIGHT`**      |         |
| **`NEWT_KEY_BKSPC`**      |         |
| **`NEWT_KEY_DELETE`**     |         |
| **`NEWT_KEY_HOME`**       |         |
| **`NEWT_KEY_END`**        |         |
| **`NEWT_KEY_UNTAB`**      |         |
| **`NEWT_KEY_PGUP`**       |         |
| **`NEWT_KEY_PGDN`**       |         |
| **`NEWT_KEY_INSERT`**     |         |
| **`NEWT_KEY_F1`**         |         |
| **`NEWT_KEY_F2`**         |         |
| **`NEWT_KEY_F3`**         |         |
| **`NEWT_KEY_F4`**         |         |
| **`NEWT_KEY_F5`**         |         |
| **`NEWT_KEY_F6`**         |         |
| **`NEWT_KEY_F7`**         |         |
| **`NEWT_KEY_F8`**         |         |
| **`NEWT_KEY_F9`**         |         |
| **`NEWT_KEY_F10`**        |         |
| **`NEWT_KEY_F11`**        |         |
| **`NEWT_KEY_F12`**        |         |
| **`NEWT_KEY_RESIZE`**     |         |

Newt Anchors
------------

| constant                 | meaning |
|--------------------------|---------|
| **`NEWT_ANCHOR_LEFT`**   |         |
| **`NEWT_ANCHOR_RIGHT`**  |         |
| **`NEWT_ANCHOR_TOP`**    |         |
| **`NEWT_ANCHOR_BOTTOM`** |         |

Grid Flags
----------

| constant                   | meaning |
|----------------------------|---------|
| **`NEWT_GRID_FLAG_GROWX`** |         |
| **`NEWT_GRID_FLAG_GROWY`** |         |
| **`NEWT_GRID_EMPTY`**      |         |
| **`NEWT_GRID_COMPONENT`**  |         |
| **`NEWT_GRID_SUBGRID`**    |         |
