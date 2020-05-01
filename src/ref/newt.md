newt\_bell
==========

Send a beep to the terminal

### 说明

<span class="type">void</span> <span
class="methodname">newt\_bell</span> ( <span
class="methodparam">void</span> )

This function sends a beep to the terminal.

> **Note**:
>
> Depending on the terminal's settings, this beep may or may not be
> audible.

### 返回值

没有返回值。

newt\_button\_bar
=================

This function returns a grid containing the buttons created

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_button\_bar</span> ( <span
class="methodparam"><span class="type">array</span> `&$buttons`</span> )

This function returns a grid containing the buttons created.

### 参数

`buttons`  

### 返回值

Returns grid containing the buttons created.

newt\_button
============

Create a new button

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_button</span> ( <span class="methodparam"><span
class="type">int</span> `$left`</span> , <span class="methodparam"><span
class="type">int</span> `$top`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> )

Creates a new button.

### 参数

`left`  
X-coordinate of the button.

`top`  
Y-coordinate of the button.

`text`  
The text which should be displayed in the button.

### 返回值

Returns a resource link to the created button component, or **`FALSE`**
on error.

### 范例

**示例 \#1 A <span class="function">newt\_button</span> example**

``` php
<?php

$form = newt_form();

$ok_button = newt_button(5, 12, "Run Tool");
    
newt_form_add_component($form, $ok_button);

?>
```

### 参见

-   <span class="function">newt\_button\_bar</span>

newt\_centered\_window
======================

Open a centered window of the specified size

### 说明

<span class="type">int</span> <span
class="methodname">newt\_centered\_window</span> ( <span
class="methodparam"><span class="type">int</span> `$width`</span> ,
<span class="methodparam"><span class="type">int</span> `$height`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$title`</span> \] )

Open a centered window of the specified size.

### 参数

`width`  
Window width

`height`  
Window height

`title`  
Window title

### 返回值

Undefined value.

### 参见

-   <span class="function">newt\_pop\_window</span>
-   <span class="function">newt\_open\_window</span>

newt\_checkbox\_get\_value
==========================

Retreives value of checkox resource

### 说明

<span class="type">string</span> <span
class="methodname">newt\_checkbox\_get\_value</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkbox`</span> )

This function returns the character in the sequence which indicates the
current value of the checkbox.

### 参数

`checkbox`  

### 返回值

Returns character indicating the value of the checkbox.

newt\_checkbox\_set\_flags
==========================

Configures checkbox resource

### 说明

<span class="type">void</span> <span
class="methodname">newt\_checkbox\_set\_flags</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkbox`</span> , <span class="methodparam"><span
class="type">int</span> `$flags`</span> , <span
class="methodparam"><span class="type">int</span> `$sense`</span> )

This function allows to set various flags on checkbox resource.

### 参数

`checkbox`  

`flags`  

`sense`  

### 返回值

没有返回值。

newt\_checkbox\_set\_value
==========================

Sets the value of the checkbox

### 说明

<span class="type">void</span> <span
class="methodname">newt\_checkbox\_set\_value</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkbox`</span> , <span class="methodparam"><span
class="type">string</span> `$value`</span> )

This function allows to set the current value of the checkbox resource.

### 参数

`checkbox`  

`value`  

### 返回值

没有返回值。

newt\_checkbox\_tree\_add\_item
===============================

Adds new item to the checkbox tree

### 说明

<span class="type">void</span> <span
class="methodname">newt\_checkbox\_tree\_add\_item</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> , <span
class="methodparam"><span class="type">mixed</span> `$data`</span> ,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
, <span class="methodparam"><span class="type">int</span>
`$index`</span> \[, <span class="methodparam"><span
class="type">int</span> `$...`</span> \] )

This function allows to add new item to the checkbox tree.

### 参数

`checkboxtree`  

`text`  

`data`  

`flags`  

`index`  

### 返回值

没有返回值。

newt\_checkbox\_tree\_find\_item
================================

Finds an item in the checkbox tree

### 说明

<span class="type">array</span> <span
class="methodname">newt\_checkbox\_tree\_find\_item</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> )

Finds an item in the checkbox tree by item's data.

### 参数

`checkboxtree`  

`data`  

### 返回值

Returns checkbox tree item resource, or **`NULL`** if it wasn't found.

newt\_checkbox\_tree\_get\_current
==================================

Returns checkbox tree selected item

### 说明

<span class="type">mixed</span> <span
class="methodname">newt\_checkbox\_tree\_get\_current</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> )

This method returns checkbox tree selected tem.

### 参数

`checkboxtree`  

### 返回值

Returns current (selected) checkbox tree item.

newt\_checkbox\_tree\_get\_entry\_value
=======================================

### 说明

<span class="type">string</span> <span
class="methodname">newt\_checkbox\_tree\_get\_entry\_value</span> (
<span class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`checkboxtree`  

`data`  

### 返回值

newt\_checkbox\_tree\_get\_multi\_selection
===========================================

### 说明

<span class="type">array</span> <span
class="methodname">newt\_checkbox\_tree\_get\_multi\_selection</span> (
<span class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> , <span class="methodparam"><span
class="type">string</span> `$seqnum`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`checkboxtree`  

`seqnum`  

### 返回值

newt\_checkbox\_tree\_get\_selection
====================================

### 说明

<span class="type">array</span> <span
class="methodname">newt\_checkbox\_tree\_get\_selection</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`checkboxtree`  

### 返回值

newt\_checkbox\_tree\_multi
===========================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_checkbox\_tree\_multi</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">int</span> `$height`</span> ,
<span class="methodparam"><span class="type">string</span> `$seq`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`height`  

`seq`  

`flags`  

### 返回值

newt\_checkbox\_tree\_set\_current
==================================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_checkbox\_tree\_set\_current</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`checkboxtree`  

`data`  

### 返回值

没有返回值。

newt\_checkbox\_tree\_set\_entry\_value
=======================================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_checkbox\_tree\_set\_entry\_value</span> (
<span class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> , <span
class="methodparam"><span class="type">string</span> `$value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`checkboxtree`  

`data`  

`value`  

### 返回值

没有返回值。

newt\_checkbox\_tree\_set\_entry
================================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_checkbox\_tree\_set\_entry</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkboxtree`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`checkboxtree`  

`data`  

`text`  

### 返回值

没有返回值。

newt\_checkbox\_tree\_set\_width
================================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_checkbox\_tree\_set\_width</span> ( <span
class="methodparam"><span class="type">resource</span>
`$checkbox_tree`</span> , <span class="methodparam"><span
class="type">int</span> `$width`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`checkbox_tree`  

`width`  

### 返回值

没有返回值。

newt\_checkbox\_tree
====================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_checkbox\_tree</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">int</span> `$height`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`height`  

`flags`  

### 返回值

newt\_checkbox
==============

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_checkbox</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">string</span>
`$def_value`</span> \[, <span class="methodparam"><span
class="type">string</span> `$seq`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`text`  

`def_value`  

`seq`  

### 返回值

newt\_clear\_key\_buffer
========================

Discards the contents of the terminal's input buffer without waiting for
additional input

### 说明

<span class="type">void</span> <span
class="methodname">newt\_clear\_key\_buffer</span> ( <span
class="methodparam">void</span> )

Discards the contents of the terminal's input buffer without waiting for
additional input.

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_wait\_for\_key</span>

newt\_cls
=========

### 说明

<span class="type">void</span> <span class="methodname">newt\_cls</span>
( <span class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

### 返回值

没有返回值。

newt\_compact\_button
=====================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_compact\_button</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`text`  

### 返回值

newt\_component\_add\_callback
==============================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_component\_add\_callback</span> ( <span
class="methodparam"><span class="type">resource</span>
`$component`</span> , <span class="methodparam"><span
class="type">mixed</span> `$func_name`</span> , <span
class="methodparam"><span class="type">mixed</span> `$data`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`component`  

`func_name`  

`data`  

### 返回值

没有返回值。

newt\_component\_takes\_focus
=============================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_component\_takes\_focus</span> ( <span
class="methodparam"><span class="type">resource</span>
`$component`</span> , <span class="methodparam"><span
class="type">bool</span> `$takes_focus`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`component`  

`takes_focus`  

### 返回值

没有返回值。

newt\_create\_grid
==================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_create\_grid</span> ( <span
class="methodparam"><span class="type">int</span> `$cols`</span> , <span
class="methodparam"><span class="type">int</span> `$rows`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`cols`  

`rows`  

### 返回值

newt\_cursor\_off
=================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_cursor\_off</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

### 返回值

没有返回值。

newt\_cursor\_on
================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_cursor\_on</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 返回值

没有返回值。

newt\_delay
===========

### 说明

<span class="type">void</span> <span
class="methodname">newt\_delay</span> ( <span class="methodparam"><span
class="type">int</span> `$microseconds`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`microseconds`  

### 返回值

没有返回值。

newt\_draw\_form
================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_draw\_form</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`form`  

### 返回值

没有返回值。

newt\_draw\_root\_text
======================

Displays the string text at the position indicated

### 说明

<span class="type">void</span> <span
class="methodname">newt\_draw\_root\_text</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> )

Displays the string text at the position indicated.

### 参数

`left`  
Column number

> **Note**:
>
> If left is negative, the position is measured from the opposite side
> of the screen.

`top`  
Line number

> **Note**:
>
> If top is negative, the position is measured from the opposite side of
> the screen.

`text`  
Text to display.

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">newt\_draw\_root\_text</span>
example**

This code demonstrates drawing of titles in the both corners of the
screen.

``` php
<?php
 newt_init();
 newt_cls();

 newt_draw_root_text (2, 0, "Some root text");
 newt_refresh();
 sleep(1);

 newt_draw_root_text (-30, 0, "Root text in the other corner");
 newt_refresh();
 sleep(1);

 newt_finished();
?>
```

### 参见

-   <span class="function">newt\_push\_help\_line</span>
-   <span class="function">newt\_pop\_help\_line</span>

newt\_entry\_get\_value
=======================

### 说明

<span class="type">string</span> <span
class="methodname">newt\_entry\_get\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$entry`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`entry`  

### 返回值

newt\_entry\_set\_filter
========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_entry\_set\_filter</span> ( <span
class="methodparam"><span class="type">resource</span> `$entry`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$filter`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`entry`  

`filter`  

`data`  

### 返回值

没有返回值。

newt\_entry\_set\_flags
=======================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_entry\_set\_flags</span> ( <span
class="methodparam"><span class="type">resource</span> `$entry`</span> ,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
, <span class="methodparam"><span class="type">int</span>
`$sense`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`entry`  

`flags`  

`sense`  

### 返回值

没有返回值。

newt\_entry\_set
================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_entry\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$entry`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> \[, <span class="methodparam"><span
class="type">bool</span> `$cursor_at_end`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`entry`  

`value`  

`cursor_at_end`  

### 返回值

没有返回值。

newt\_entry
===========

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_entry</span> ( <span class="methodparam"><span
class="type">int</span> `$left`</span> , <span class="methodparam"><span
class="type">int</span> `$top`</span> , <span class="methodparam"><span
class="type">int</span> `$width`</span> \[, <span
class="methodparam"><span class="type">string</span>
`$init_value`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`width`  

`init_value`  

`flags`  

### 返回值

newt\_finished
==============

Uninitializes newt interface

### 说明

<span class="type">int</span> <span
class="methodname">newt\_finished</span> ( <span
class="methodparam">void</span> )

Uninitializes newt interface. This function be called, when program is
ready to exit.

### 返回值

Returns 1 on success, 0 on failure.

### 参见

-   <span class="function">newt\_init</span>

newt\_form\_add\_component
==========================

Adds a single component to the form

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_add\_component</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$component`</span> )

Adds a single component to the `form`.

### 参数

`form`  
Form to which component will be added

`component`  
Component to add to the form

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">newt\_form\_add\_component</span>
example**

``` php
<?php
$form = newt_form();

$options = array("Authentication configuration", "Firewall configuration",
"Mouse configuration", "Network configuration", "Printer configuration",
"System services");

$list = newt_listbox(3, 2, 10);

foreach ($options as $l_item) {
    newt_listbox_add_entry($list, $l_item, $l_item);
}

newt_form_add_component($form, $list);
?>
```

### 参见

-   <span class="function">newt\_form\_add\_components</span>

newt\_form\_add\_components
===========================

Add several components to the form

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_add\_components</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> ,
<span class="methodparam"><span class="type">array</span>
`$components`</span> )

Adds several components to the `form`.

### 参数

`form`  
Form to which components will be added

`components`  
Array of components to add to the form

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">newt\_form\_add\_components</span>
example**

``` php
<?php
$form = newt_form();

$b1 = newt_button(5, 12, "Run Tool");
$b2 = newt_button(21, 12, "Quit");

newt_form_add_components($form, array($b1, $b2));
?>
```

### 参见

-   <span class="function">newt\_form\_add\_component</span>

newt\_form\_add\_hot\_key
=========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_add\_hot\_key</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> ,
<span class="methodparam"><span class="type">int</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`form`  

`key`  

### 返回值

没有返回值。

newt\_form\_destroy
===================

Destroys a form

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_destroy</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> )

This function frees the memory resources used by the form and all of the
components which have been added to the form (including those components
which are on subforms). Once a form has been destroyed, none of the
form's components can be used.

### 参数

`form`  
Form component, which is going to be destroyed

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_form\_run</span>
-   <span class="function">newt\_run\_form</span>

newt\_form\_get\_current
========================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_form\_get\_current</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`form`  

### 返回值

newt\_form\_run
===============

Runs a form

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_run</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> ,
<span class="methodparam"><span class="type">array</span>
`&$exit_struct`</span> )

This function runs the form passed to it.

### 参数

`form`  
Form component

`exit_struct`  
Array, used for returning information after running the form component.
Keys and values are described in the following table:

| Index Key | Value Type | Description                                                                                                                                              |
|-----------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| reason    | integer    | The reason, why the form has been exited. Possible values are defined <a href="/newt/constants.html#Newt%20form%20exit%20reasons" class="link">here</a>. |
| watch     | resource   | Resource link, specified in <span class="function">newt\_form\_watch\_fd</span>                                                                          |
| key       | integer    | Hotkey                                                                                                                                                   |
| component | resource   | Component, which caused the form to exit                                                                                                                 |

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_run\_form</span>

newt\_form\_set\_background
===========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_set\_background</span> ( <span
class="methodparam"><span class="type">resource</span> `$from`</span> ,
<span class="methodparam"><span class="type">int</span>
`$background`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`from`  

`background`  

### 返回值

没有返回值。

newt\_form\_set\_height
=======================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_set\_height</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> ,
<span class="methodparam"><span class="type">int</span> `$height`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`form`  

`height`  

### 返回值

没有返回值。

newt\_form\_set\_size
=====================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_set\_size</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`form`  

### 返回值

没有返回值。

newt\_form\_set\_timer
======================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_set\_timer</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> ,
<span class="methodparam"><span class="type">int</span>
`$milliseconds`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`form`  

`milliseconds`  

### 返回值

没有返回值。

newt\_form\_set\_width
======================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_set\_width</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`form`  

`width`  

### 返回值

没有返回值。

newt\_form\_watch\_fd
=====================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_form\_watch\_fd</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$stream`</span> \[, <span class="methodparam"><span
class="type">int</span> `$flags`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`form`  

`stream`  

`flags`  

### 返回值

没有返回值。

newt\_form
==========

Create a form

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_form</span> (\[ <span class="methodparam"><span
class="type">resource</span> `$vert_bar`</span> \[, <span
class="methodparam"><span class="type">string</span> `$help`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\]\]\] )

Create a new form.

### 参数

`vert_bar`  
Vertical scrollbar which should be associated with the form

`help`  
Help text string

`flags`  
Various flags

### 返回值

Returns a resource link to the created form component, or **`FALSE`** on
error.

### 范例

**示例 \#1 A <span class="function">newt\_form</span> example**

Displays a single button "Quit", which closes the application once it's
pressed.

``` php
<?php
newt_init();
newt_cls();

$myform = newt_form();
$button = newt_button (5, 12, "Quit");

newt_form_add_component ($myform, $button);
newt_refresh ();
newt_run_form ($myform);

newt_finished ();
newt_form_destroy ($myform);
?>
```

### 参见

-   <span class="function">newt\_form\_run</span>
-   <span class="function">newt\_run\_form</span>
-   <span class="function">newt\_form\_add\_component</span>
-   <span class="function">newt\_form\_add\_components</span>
-   <span class="function">newt\_form\_destroy</span>

newt\_get\_screen\_size
=======================

Fills in the passed references with the current size of the terminal

### 说明

<span class="type">void</span> <span
class="methodname">newt\_get\_screen\_size</span> ( <span
class="methodparam"><span class="type">int</span> `&$cols`</span> ,
<span class="methodparam"><span class="type">int</span> `&$rows`</span>
)

Fills in the passed references with the current size of the terminal.

### 参数

`cols`  
Number of columns in the terminal

`rows`  
Number of rows in the terminal

### 返回值

没有返回值。

### 范例

**示例 \#1 A <span class="function">newt\_get\_screen\_size</span>
example**

This code prints out the screen size of your terminal.

``` php
<?php
 newt_init();
 newt_get_screen_size (&$cols, &$rows);
 newt_finished();

 print "Your terminal size is: {$cols}x{$rows}\n";
?>
```

以上例程会输出：

    Your terminal size is: 138x47

newt\_grid\_add\_components\_to\_form
=====================================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_grid\_add\_components\_to\_form</span> ( <span
class="methodparam"><span class="type">resource</span> `$grid`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$form`</span> , <span class="methodparam"><span
class="type">bool</span> `$recurse`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`grid`  

`form`  

`recurse`  

### 返回值

没有返回值。

newt\_grid\_basic\_window
=========================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_grid\_basic\_window</span> ( <span
class="methodparam"><span class="type">resource</span> `$text`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$middle`</span> , <span class="methodparam"><span
class="type">resource</span> `$buttons`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`text`  

`middle`  

`buttons`  

### 返回值

newt\_grid\_free
================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_grid\_free</span> ( <span
class="methodparam"><span class="type">resource</span> `$grid`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$recurse`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`grid`  

`recurse`  

### 返回值

没有返回值。

newt\_grid\_get\_size
=====================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_grid\_get\_size</span> ( <span
class="methodparam"><span class="type">resouce</span> `$grid`</span> ,
<span class="methodparam"><span class="type">int</span> `&$width`</span>
, <span class="methodparam"><span class="type">int</span>
`&$height`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`grid`  

`width`  

`height`  

### 返回值

没有返回值。

newt\_grid\_h\_close\_stacked
=============================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_grid\_h\_close\_stacked</span> ( <span
class="methodparam"><span class="type">int</span>
`$element1_type`</span> , <span class="methodparam"><span
class="type">resource</span> `$element1`</span> \[, <span
class="methodparam"><span class="type">int</span> `$...`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$...`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`element1_type`  

`element1`  

### 返回值

newt\_grid\_h\_stacked
======================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_grid\_h\_stacked</span> ( <span
class="methodparam"><span class="type">int</span>
`$element1_type`</span> , <span class="methodparam"><span
class="type">resource</span> `$element1`</span> \[, <span
class="methodparam"><span class="type">int</span> `$...`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$...`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`element1_type`  

`element1`  

### 返回值

newt\_grid\_place
=================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_grid\_place</span> ( <span
class="methodparam"><span class="type">resource</span> `$grid`</span> ,
<span class="methodparam"><span class="type">int</span> `$left`</span> ,
<span class="methodparam"><span class="type">int</span> `$top`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`grid`  

`left`  

`top`  

### 返回值

没有返回值。

newt\_grid\_set\_field
======================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_grid\_set\_field</span> ( <span
class="methodparam"><span class="type">resource</span> `$grid`</span> ,
<span class="methodparam"><span class="type">int</span> `$col`</span> ,
<span class="methodparam"><span class="type">int</span> `$row`</span> ,
<span class="methodparam"><span class="type">int</span> `$type`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$val`</span> , <span class="methodparam"><span class="type">int</span>
`$pad_left`</span> , <span class="methodparam"><span
class="type">int</span> `$pad_top`</span> , <span
class="methodparam"><span class="type">int</span> `$pad_right`</span> ,
<span class="methodparam"><span class="type">int</span>
`$pad_bottom`</span> , <span class="methodparam"><span
class="type">int</span> `$anchor`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`grid`  

`col`  

`row`  

`type`  

`val`  

`pad_left`  

`pad_top`  

`pad_right`  

`pad_bottom`  

`anchor`  

`flags`  

### 返回值

没有返回值。

newt\_grid\_simple\_window
==========================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_grid\_simple\_window</span> ( <span
class="methodparam"><span class="type">resource</span> `$text`</span> ,
<span class="methodparam"><span class="type">resource</span>
`$middle`</span> , <span class="methodparam"><span
class="type">resource</span> `$buttons`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`text`  

`middle`  

`buttons`  

### 返回值

newt\_grid\_v\_close\_stacked
=============================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_grid\_v\_close\_stacked</span> ( <span
class="methodparam"><span class="type">int</span>
`$element1_type`</span> , <span class="methodparam"><span
class="type">resource</span> `$element1`</span> \[, <span
class="methodparam"><span class="type">int</span> `$...`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$...`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`element1_type`  

`element1`  

### 返回值

newt\_grid\_v\_stacked
======================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_grid\_v\_stacked</span> ( <span
class="methodparam"><span class="type">int</span>
`$element1_type`</span> , <span class="methodparam"><span
class="type">resource</span> `$element1`</span> \[, <span
class="methodparam"><span class="type">int</span> `$...`</span> \[,
<span class="methodparam"><span class="type">resource</span>
`$...`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`element1_type`  

`element1`  

### 返回值

newt\_grid\_wrapped\_window\_at
===============================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_grid\_wrapped\_window\_at</span> ( <span
class="methodparam"><span class="type">resource</span> `$grid`</span> ,
<span class="methodparam"><span class="type">string</span>
`$title`</span> , <span class="methodparam"><span
class="type">int</span> `$left`</span> , <span class="methodparam"><span
class="type">int</span> `$top`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`grid`  

`title`  

`left`  

`top`  

### 返回值

没有返回值。

newt\_grid\_wrapped\_window
===========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_grid\_wrapped\_window</span> ( <span
class="methodparam"><span class="type">resource</span> `$grid`</span> ,
<span class="methodparam"><span class="type">string</span>
`$title`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`grid`  

`title`  

### 返回值

没有返回值。

newt\_init
==========

Initialize newt

### 说明

<span class="type">int</span> <span class="methodname">newt\_init</span>
( <span class="methodparam">void</span> )

Initializes the newt interface. This function must be called before any
other newt function.

### 返回值

Returns 1 on success, 0 on failure.

### 参见

-   <span class="function">newt\_finished</span>

newt\_label\_set\_text
======================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_label\_set\_text</span> ( <span
class="methodparam"><span class="type">resource</span> `$label`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`label`  

`text`  

### 返回值

没有返回值。

newt\_label
===========

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_label</span> ( <span class="methodparam"><span
class="type">int</span> `$left`</span> , <span class="methodparam"><span
class="type">int</span> `$top`</span> , <span class="methodparam"><span
class="type">string</span> `$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`text`  

### 返回值

newt\_listbox\_append\_entry
============================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_append\_entry</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`text`  

`data`  

### 返回值

没有返回值。

newt\_listbox\_clear\_selection
===============================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_clear\_selection</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

### 返回值

没有返回值。

newt\_listbox\_clear
====================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_clear</span> ( <span
class="methodparam"><span class="type">resource</span> `$listobx`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listobx`  

### 返回值

没有返回值。

newt\_listbox\_delete\_entry
============================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_delete\_entry</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`key`  

### 返回值

没有返回值。

newt\_listbox\_get\_current
===========================

### 说明

<span class="type">string</span> <span
class="methodname">newt\_listbox\_get\_current</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

### 返回值

newt\_listbox\_get\_selection
=============================

### 说明

<span class="type">array</span> <span
class="methodname">newt\_listbox\_get\_selection</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

### 返回值

newt\_listbox\_insert\_entry
============================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_insert\_entry</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> , <span
class="methodparam"><span class="type">mixed</span> `$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`text`  

`data`  

`key`  

### 返回值

没有返回值。

newt\_listbox\_item\_count
==========================

### 说明

<span class="type">int</span> <span
class="methodname">newt\_listbox\_item\_count</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

### 返回值

newt\_listbox\_select\_item
===========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_select\_item</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$key`</span> , <span class="methodparam"><span class="type">int</span>
`$sense`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`key`  

`sense`  

### 返回值

没有返回值。

newt\_listbox\_set\_current\_by\_key
====================================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_set\_current\_by\_key</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$key`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`key`  

### 返回值

没有返回值。

newt\_listbox\_set\_current
===========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_set\_current</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">int</span> `$num`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`num`  

### 返回值

没有返回值。

newt\_listbox\_set\_data
========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_set\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">int</span> `$num`</span>
, <span class="methodparam"><span class="type">mixed</span>
`$data`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`num`  

`data`  

### 返回值

没有返回值。

newt\_listbox\_set\_entry
=========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_set\_entry</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">int</span> `$num`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`num`  

`text`  

### 返回值

没有返回值。

newt\_listbox\_set\_width
=========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listbox\_set\_width</span> ( <span
class="methodparam"><span class="type">resource</span> `$listbox`</span>
, <span class="methodparam"><span class="type">int</span>
`$width`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`listbox`  

`width`  

### 返回值

没有返回值。

newt\_listbox
=============

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_listbox</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">int</span> `$height`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`height`  

`flags`  

### 返回值

newt\_listitem\_get\_data
=========================

### 说明

<span class="type">mixed</span> <span
class="methodname">newt\_listitem\_get\_data</span> ( <span
class="methodparam"><span class="type">resource</span> `$item`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`item`  

### 返回值

newt\_listitem\_set
===================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_listitem\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$item`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`item`  

`text`  

### 返回值

没有返回值。

newt\_listitem
==============

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_listitem</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$is_default`</span> , <span class="methodparam"><span
class="type">resouce</span> `$prev_item`</span> , <span
class="methodparam"><span class="type">mixed</span> `$data`</span> \[,
<span class="methodparam"><span class="type">int</span> `$flags`</span>
\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`text`  

`is_default`  

`prev_item`  

`data`  

`flags`  

### 返回值

newt\_open\_window
==================

Open a window of the specified size and position

### 说明

<span class="type">int</span> <span
class="methodname">newt\_open\_window</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">int</span> `$width`</span> ,
<span class="methodparam"><span class="type">int</span> `$height`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$title`</span> \] )

Open a window of the specified size and position.

### 参数

`left`  
Location of the upper left-hand corner of the window (column number)

`top`  
Location of the upper left-hand corner of the window (row number)

`width`  
Window width

`height`  
Window height

`title`  
Window title

### 返回值

Returns 1 on success, 0 on failure.

### 参见

-   <span class="function">newt\_pop\_window</span>
-   <span class="function">newt\_centered\_window</span>

newt\_pop\_help\_line
=====================

Replaces the current help line with the one from the stack

### 说明

<span class="type">void</span> <span
class="methodname">newt\_pop\_help\_line</span> ( <span
class="methodparam">void</span> )

Replaces the current help line with the one from the stack.

> **Note**:
>
> It's important not to call to <span
> class="function">newt\_pop\_help\_line</span> more than <span
> class="function">newt\_push\_help\_line</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_push\_help\_line</span>

newt\_pop\_window
=================

Removes the top window from the display

### 说明

<span class="type">void</span> <span
class="methodname">newt\_pop\_window</span> ( <span
class="methodparam">void</span> )

Removes the top window from the display, and redraws the display areas
which the window overwrote.

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_open\_window</span>
-   <span class="function">newt\_centered\_window</span>

newt\_push\_help\_line
======================

Saves the current help line on a stack, and displays the new line

### 说明

<span class="type">void</span> <span
class="methodname">newt\_push\_help\_line</span> (\[ <span
class="methodparam"><span class="type">string</span> `$text`</span> \] )

Saves the current help line on a stack, and displays the new line.

### 参数

`text`  
New help text message

> **Note**:
>
> If not specified, the help line is cleared.

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_pop\_help\_line</span>

newt\_radio\_get\_current
=========================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_radio\_get\_current</span> ( <span
class="methodparam"><span class="type">resource</span>
`$set_member`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`set_member`  

### 返回值

newt\_radiobutton
=================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_radiobutton</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">bool</span>
`$is_default`</span> \[, <span class="methodparam"><span
class="type">resource</span> `$prev_button`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`text`  

`is_default`  

`prev_button`  

### 返回值

newt\_redraw\_help\_line
========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_redraw\_help\_line</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

### 返回值

没有返回值。

newt\_reflow\_text
==================

### 说明

<span class="type">string</span> <span
class="methodname">newt\_reflow\_text</span> ( <span
class="methodparam"><span class="type">string</span> `$text`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
, <span class="methodparam"><span class="type">int</span>
`$flex_down`</span> , <span class="methodparam"><span
class="type">int</span> `$flex_up`</span> , <span
class="methodparam"><span class="type">int</span>
`&$actual_width`</span> , <span class="methodparam"><span
class="type">int</span> `&$actual_height`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`text`  

`width`  

`flex_down`  

`flex_up`  

`actual_width`  

`actual_height`  

### 返回值

newt\_refresh
=============

Updates modified portions of the screen

### 说明

<span class="type">void</span> <span
class="methodname">newt\_refresh</span> ( <span
class="methodparam">void</span> )

To increase performance, newt only updates the display when it needs to,
not when the program tells it to write to the terminal. Applications can
force newt to immediately update modified portions of the screen by
calling this function.

### 返回值

没有返回值。

newt\_resize\_screen
====================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_resize\_screen</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$redraw`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`redraw`  

### 返回值

没有返回值。

newt\_resume
============

Resume using the newt interface after calling <span
class="function">newt\_suspend</span>

### 说明

<span class="type">void</span> <span
class="methodname">newt\_resume</span> ( <span
class="methodparam">void</span> )

Resume using the newt interface after calling <span
class="function">newt\_suspend</span>.

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_suspend</span>

newt\_run\_form
===============

Runs a form

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_run\_form</span> ( <span
class="methodparam"><span class="type">resource</span> `$form`</span> )

This function runs the form passed to it.

### 参数

`form`  
Form component

### 返回值

The component which caused the form to stop running.

> **Note**:
>
> Notice that this function doesn't fit in with newt's normal naming
> convention. It is an older interface which will not work for all
> forms. It was left in newt only for legacy applications. It is a
> simpler interface than the new <span
> class="function">newt\_form\_run</span> though, and is still used
> quite often as a result. When an application is done with a form, it
> destroys the form and all of the components the form contains.

### 参见

-   <span class="function">newt\_form\_run</span>
-   <span class="function">newt\_form\_destroy</span>

newt\_scale\_set
================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_scale\_set</span> ( <span
class="methodparam"><span class="type">resource</span> `$scale`</span> ,
<span class="methodparam"><span class="type">int</span> `$amount`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`scale`  

`amount`  

### 返回值

没有返回值。

newt\_scale
===========

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_scale</span> ( <span class="methodparam"><span
class="type">int</span> `$left`</span> , <span class="methodparam"><span
class="type">int</span> `$top`</span> , <span class="methodparam"><span
class="type">int</span> `$width`</span> , <span
class="methodparam"><span class="type">int</span> `$full_value`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`width`  

`full_value`  

### 返回值

newt\_scrollbar\_set
====================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_scrollbar\_set</span> ( <span
class="methodparam"><span class="type">resource</span>
`$scrollbar`</span> , <span class="methodparam"><span
class="type">int</span> `$where`</span> , <span
class="methodparam"><span class="type">int</span> `$total`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`scrollbar`  

`where`  

`total`  

### 返回值

没有返回值。

newt\_set\_help\_callback
=========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_set\_help\_callback</span> ( <span
class="methodparam"><span class="type">mixed</span> `$function`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`function`  

### 返回值

没有返回值。

newt\_set\_suspend\_callback
============================

Set a callback function which gets invoked when user presses the suspend
key

### 说明

<span class="type">void</span> <span
class="methodname">newt\_set\_suspend\_callback</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> , <span class="methodparam"><span
class="type">mixed</span> `$data`</span> )

Set a callback function which gets invoked when user presses the suspend
key (normally ^Z). If no suspend callback is registered, the suspend
keystroke is ignored.

### 参数

`function`  
A callback function, which accepts one argument: data

`data`  
This data is been passed to the callback function

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_suspend</span>
-   <span class="function">newt\_resume</span>

newt\_suspend
=============

Tells newt to return the terminal to its initial state

### 说明

<span class="type">void</span> <span
class="methodname">newt\_suspend</span> ( <span
class="methodparam">void</span> )

Tells newt to return the terminal to its initial state. Once this is
done, the application can suspend itself (by sending itself a SIGTSTP,
fork a child program, or do whatever else it likes).

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_resume</span>

newt\_textbox\_get\_num\_lines
==============================

### 说明

<span class="type">int</span> <span
class="methodname">newt\_textbox\_get\_num\_lines</span> ( <span
class="methodparam"><span class="type">resource</span> `$textbox`</span>
)

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`textbox`  

### 返回值

newt\_textbox\_reflowed
=======================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_textbox\_reflowed</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">char</span> `$*text`</span> ,
<span class="methodparam"><span class="type">int</span> `$width`</span>
, <span class="methodparam"><span class="type">int</span>
`$flex_down`</span> , <span class="methodparam"><span
class="type">int</span> `$flex_up`</span> \[, <span
class="methodparam"><span class="type">int</span> `$flags`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`*text`  

`width`  

`flex_down`  

`flex_up`  

`flags`  

### 返回值

newt\_textbox\_set\_height
==========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_textbox\_set\_height</span> ( <span
class="methodparam"><span class="type">resource</span> `$textbox`</span>
, <span class="methodparam"><span class="type">int</span>
`$height`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`textbox`  

`height`  

### 返回值

没有返回值。

newt\_textbox\_set\_text
========================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_textbox\_set\_text</span> ( <span
class="methodparam"><span class="type">resource</span> `$textbox`</span>
, <span class="methodparam"><span class="type">string</span>
`$text`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`textbox`  

`text`  

### 返回值

没有返回值。

newt\_textbox
=============

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_textbox</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">int</span> `$width`</span> ,
<span class="methodparam"><span class="type">int</span> `$height`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$flags`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`width`  

`height`  

`flags`  

### 返回值

newt\_vertical\_scrollbar
=========================

### 说明

<span class="type">resource</span> <span
class="methodname">newt\_vertical\_scrollbar</span> ( <span
class="methodparam"><span class="type">int</span> `$left`</span> , <span
class="methodparam"><span class="type">int</span> `$top`</span> , <span
class="methodparam"><span class="type">int</span> `$height`</span> \[,
<span class="methodparam"><span class="type">int</span>
`$normal_colorset`</span> \[, <span class="methodparam"><span
class="type">int</span> `$thumb_colorset`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`left`  

`top`  

`height`  

`normal_colorset`  

`thumb_colorset`  

### 返回值

newt\_wait\_for\_key
====================

Doesn't return until a key has been pressed

### 说明

<span class="type">void</span> <span
class="methodname">newt\_wait\_for\_key</span> ( <span
class="methodparam">void</span> )

This function doesn't return until a key has been pressed. The keystroke
is then ignored. If a key is already in the terminal's buffer, this
function discards a keystroke and returns immediately.

### 返回值

没有返回值。

### 参见

-   <span class="function">newt\_clear\_key\_buffer</span>

newt\_win\_choice
=================

### 说明

<span class="type">int</span> <span
class="methodname">newt\_win\_choice</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> ,
<span class="methodparam"><span class="type">string</span>
`$button1_text`</span> , <span class="methodparam"><span
class="type">string</span> `$button2_text`</span> , <span
class="methodparam"><span class="type">string</span> `$format`</span>
\[, <span class="methodparam"><span class="type">mixed</span>
`$args`</span> \[, <span class="methodparam"><span
class="type">mixed</span> `$...`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`title`  

`button1_text`  

`button2_text`  

`format`  

`args`  

### 返回值

newt\_win\_entries
==================

### 说明

<span class="type">int</span> <span
class="methodname">newt\_win\_entries</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span class="type">int</span>
`$suggested_width`</span> , <span class="methodparam"><span
class="type">int</span> `$flex_down`</span> , <span
class="methodparam"><span class="type">int</span> `$flex_up`</span> ,
<span class="methodparam"><span class="type">int</span>
`$data_width`</span> , <span class="methodparam"><span
class="type">array</span> `&$items`</span> , <span
class="methodparam"><span class="type">string</span> `$button1`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$...`</span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`title`  

`text`  

`suggested_width`  

`flex_down`  

`flex_up`  

`data_width`  

`items`  

`button1`  

`button2`  

### 返回值

### 范例

**示例 \#1 A <span class="function">newt\_win\_entries</span> example**

``` php
<?php

newt_init();
newt_cls();

$entries[] = array('text' => 'First name:', 'value' => &$f_name);
$entries[] = array('text' => 'Last name:',  'value' => &$l_name);

$rc = newt_win_entries("User information", "Please enter your credentials:", 50, 7, 7, 30, $entries, "Ok", "Back");
newt_finished ();

if ($rc != 2) {
    echo "Your name is: $f_name $l_name\n";
}
?>
```

newt\_win\_menu
===============

### 说明

<span class="type">int</span> <span
class="methodname">newt\_win\_menu</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> ,
<span class="methodparam"><span class="type">string</span>
`$text`</span> , <span class="methodparam"><span class="type">int</span>
`$suggestedWidth`</span> , <span class="methodparam"><span
class="type">int</span> `$flexDown`</span> , <span
class="methodparam"><span class="type">int</span> `$flexUp`</span> ,
<span class="methodparam"><span class="type">int</span>
`$maxListHeight`</span> , <span class="methodparam"><span
class="type">array</span> `$items`</span> , <span
class="methodparam"><span class="type">int</span> `&$listItem`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$button1`</span> \[, <span class="methodparam"><span
class="type">string</span> `$...`</span> \]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`title`  

`text`  

`suggestedWidth`  

`flexDown`  

`flexUp`  

`maxListHeight`  

`items`  

`listItem`  

`button1`  

### 返回值

没有返回值。

newt\_win\_message
==================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_win\_message</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> ,
<span class="methodparam"><span class="type">string</span>
`$button_text`</span> , <span class="methodparam"><span
class="type">string</span> `$format`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$args`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`title`  

`button_text`  

`format`  

`args`  

### 返回值

没有返回值。

newt\_win\_messagev
===================

### 说明

<span class="type">void</span> <span
class="methodname">newt\_win\_messagev</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> ,
<span class="methodparam"><span class="type">string</span>
`$button_text`</span> , <span class="methodparam"><span
class="type">string</span> `$format`</span> , <span
class="methodparam"><span class="type">array</span> `$args`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`title`  

`button_text`  

`format`  

`args`  

### 返回值

没有返回值。

newt\_win\_ternary
==================

### 说明

<span class="type">int</span> <span
class="methodname">newt\_win\_ternary</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> ,
<span class="methodparam"><span class="type">string</span>
`$button1_text`</span> , <span class="methodparam"><span
class="type">string</span> `$button2_text`</span> , <span
class="methodparam"><span class="type">string</span>
`$button3_text`</span> , <span class="methodparam"><span
class="type">string</span> `$format`</span> \[, <span
class="methodparam"><span class="type">mixed</span> `$args`</span> \[,
<span class="methodparam"><span class="type">mixed</span> `$...`</span>
\]\] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`title`  
Its description

`button1_text`  
Its description

`button2_text`  
Its description

`button3_text`  
Its description

`format`  
Its description

`args`  
Its description

### 返回值

What the function returns, first on success, then on failure. See also
the &return.success; entity

**目录**

-   [newt\_bell](/ref/newt.html#newt_bell) — Send a beep to the terminal
-   [newt\_button\_bar](/ref/newt.html#newt_button_bar) — This function
    returns a grid containing the buttons created
-   [newt\_button](/ref/newt.html#newt_button) — Create a new button
-   [newt\_centered\_window](/ref/newt.html#newt_centered_window) — Open
    a centered window of the specified size
-   [newt\_checkbox\_get\_value](/ref/newt.html#newt_checkbox_get_value)
    — Retreives value of checkox resource
-   [newt\_checkbox\_set\_flags](/ref/newt.html#newt_checkbox_set_flags)
    — Configures checkbox resource
-   [newt\_checkbox\_set\_value](/ref/newt.html#newt_checkbox_set_value)
    — Sets the value of the checkbox
-   [newt\_checkbox\_tree\_add\_item](/ref/newt.html#newt_checkbox_tree_add_item)
    — Adds new item to the checkbox tree
-   [newt\_checkbox\_tree\_find\_item](/ref/newt.html#newt_checkbox_tree_find_item)
    — Finds an item in the checkbox tree
-   [newt\_checkbox\_tree\_get\_current](/ref/newt.html#newt_checkbox_tree_get_current)
    — Returns checkbox tree selected item
-   [newt\_checkbox\_tree\_get\_entry\_value](/ref/newt.html#newt_checkbox_tree_get_entry_value)
    — 说明
-   [newt\_checkbox\_tree\_get\_multi\_selection](/ref/newt.html#newt_checkbox_tree_get_multi_selection)
    — 说明
-   [newt\_checkbox\_tree\_get\_selection](/ref/newt.html#newt_checkbox_tree_get_selection)
    — 说明
-   [newt\_checkbox\_tree\_multi](/ref/newt.html#newt_checkbox_tree_multi)
    — 说明
-   [newt\_checkbox\_tree\_set\_current](/ref/newt.html#newt_checkbox_tree_set_current)
    — 说明
-   [newt\_checkbox\_tree\_set\_entry\_value](/ref/newt.html#newt_checkbox_tree_set_entry_value)
    — 说明
-   [newt\_checkbox\_tree\_set\_entry](/ref/newt.html#newt_checkbox_tree_set_entry)
    — 说明
-   [newt\_checkbox\_tree\_set\_width](/ref/newt.html#newt_checkbox_tree_set_width)
    — 说明
-   [newt\_checkbox\_tree](/ref/newt.html#newt_checkbox_tree) — 说明
-   [newt\_checkbox](/ref/newt.html#newt_checkbox) — 说明
-   [newt\_clear\_key\_buffer](/ref/newt.html#newt_clear_key_buffer) —
    Discards the contents of the terminal's input buffer without waiting
    for additional input
-   [newt\_cls](/ref/newt.html#newt_cls) — 说明
-   [newt\_compact\_button](/ref/newt.html#newt_compact_button) — 说明
-   [newt\_component\_add\_callback](/ref/newt.html#newt_component_add_callback)
    — 说明
-   [newt\_component\_takes\_focus](/ref/newt.html#newt_component_takes_focus)
    — 说明
-   [newt\_create\_grid](/ref/newt.html#newt_create_grid) — 说明
-   [newt\_cursor\_off](/ref/newt.html#newt_cursor_off) — 说明
-   [newt\_cursor\_on](/ref/newt.html#newt_cursor_on) — 说明
-   [newt\_delay](/ref/newt.html#newt_delay) — 说明
-   [newt\_draw\_form](/ref/newt.html#newt_draw_form) — 说明
-   [newt\_draw\_root\_text](/ref/newt.html#newt_draw_root_text) —
    Displays the string text at the position indicated
-   [newt\_entry\_get\_value](/ref/newt.html#newt_entry_get_value) —
    说明
-   [newt\_entry\_set\_filter](/ref/newt.html#newt_entry_set_filter) —
    说明
-   [newt\_entry\_set\_flags](/ref/newt.html#newt_entry_set_flags) —
    说明
-   [newt\_entry\_set](/ref/newt.html#newt_entry_set) — 说明
-   [newt\_entry](/ref/newt.html#newt_entry) — 说明
-   [newt\_finished](/ref/newt.html#newt_finished) — Uninitializes newt
    interface
-   [newt\_form\_add\_component](/ref/newt.html#newt_form_add_component)
    — Adds a single component to the form
-   [newt\_form\_add\_components](/ref/newt.html#newt_form_add_components)
    — Add several components to the form
-   [newt\_form\_add\_hot\_key](/ref/newt.html#newt_form_add_hot_key) —
    说明
-   [newt\_form\_destroy](/ref/newt.html#newt_form_destroy) — Destroys a
    form
-   [newt\_form\_get\_current](/ref/newt.html#newt_form_get_current) —
    说明
-   [newt\_form\_run](/ref/newt.html#newt_form_run) — Runs a form
-   [newt\_form\_set\_background](/ref/newt.html#newt_form_set_background)
    — 说明
-   [newt\_form\_set\_height](/ref/newt.html#newt_form_set_height) —
    说明
-   [newt\_form\_set\_size](/ref/newt.html#newt_form_set_size) — 说明
-   [newt\_form\_set\_timer](/ref/newt.html#newt_form_set_timer) — 说明
-   [newt\_form\_set\_width](/ref/newt.html#newt_form_set_width) — 说明
-   [newt\_form\_watch\_fd](/ref/newt.html#newt_form_watch_fd) — 说明
-   [newt\_form](/ref/newt.html#newt_form) — Create a form
-   [newt\_get\_screen\_size](/ref/newt.html#newt_get_screen_size) —
    Fills in the passed references with the current size of the terminal
-   [newt\_grid\_add\_components\_to\_form](/ref/newt.html#newt_grid_add_components_to_form)
    — 说明
-   [newt\_grid\_basic\_window](/ref/newt.html#newt_grid_basic_window) —
    说明
-   [newt\_grid\_free](/ref/newt.html#newt_grid_free) — 说明
-   [newt\_grid\_get\_size](/ref/newt.html#newt_grid_get_size) — 说明
-   [newt\_grid\_h\_close\_stacked](/ref/newt.html#newt_grid_h_close_stacked)
    — 说明
-   [newt\_grid\_h\_stacked](/ref/newt.html#newt_grid_h_stacked) — 说明
-   [newt\_grid\_place](/ref/newt.html#newt_grid_place) — 说明
-   [newt\_grid\_set\_field](/ref/newt.html#newt_grid_set_field) — 说明
-   [newt\_grid\_simple\_window](/ref/newt.html#newt_grid_simple_window)
    — 说明
-   [newt\_grid\_v\_close\_stacked](/ref/newt.html#newt_grid_v_close_stacked)
    — 说明
-   [newt\_grid\_v\_stacked](/ref/newt.html#newt_grid_v_stacked) — 说明
-   [newt\_grid\_wrapped\_window\_at](/ref/newt.html#newt_grid_wrapped_window_at)
    — 说明
-   [newt\_grid\_wrapped\_window](/ref/newt.html#newt_grid_wrapped_window)
    — 说明
-   [newt\_init](/ref/newt.html#newt_init) — Initialize newt
-   [newt\_label\_set\_text](/ref/newt.html#newt_label_set_text) — 说明
-   [newt\_label](/ref/newt.html#newt_label) — 说明
-   [newt\_listbox\_append\_entry](/ref/newt.html#newt_listbox_append_entry)
    — 说明
-   [newt\_listbox\_clear\_selection](/ref/newt.html#newt_listbox_clear_selection)
    — 说明
-   [newt\_listbox\_clear](/ref/newt.html#newt_listbox_clear) — 说明
-   [newt\_listbox\_delete\_entry](/ref/newt.html#newt_listbox_delete_entry)
    — 说明
-   [newt\_listbox\_get\_current](/ref/newt.html#newt_listbox_get_current)
    — 说明
-   [newt\_listbox\_get\_selection](/ref/newt.html#newt_listbox_get_selection)
    — 说明
-   [newt\_listbox\_insert\_entry](/ref/newt.html#newt_listbox_insert_entry)
    — 说明
-   [newt\_listbox\_item\_count](/ref/newt.html#newt_listbox_item_count)
    — 说明
-   [newt\_listbox\_select\_item](/ref/newt.html#newt_listbox_select_item)
    — 说明
-   [newt\_listbox\_set\_current\_by\_key](/ref/newt.html#newt_listbox_set_current_by_key)
    — 说明
-   [newt\_listbox\_set\_current](/ref/newt.html#newt_listbox_set_current)
    — 说明
-   [newt\_listbox\_set\_data](/ref/newt.html#newt_listbox_set_data) —
    说明
-   [newt\_listbox\_set\_entry](/ref/newt.html#newt_listbox_set_entry) —
    说明
-   [newt\_listbox\_set\_width](/ref/newt.html#newt_listbox_set_width) —
    说明
-   [newt\_listbox](/ref/newt.html#newt_listbox) — 说明
-   [newt\_listitem\_get\_data](/ref/newt.html#newt_listitem_get_data) —
    说明
-   [newt\_listitem\_set](/ref/newt.html#newt_listitem_set) — 说明
-   [newt\_listitem](/ref/newt.html#newt_listitem) — 说明
-   [newt\_open\_window](/ref/newt.html#newt_open_window) — Open a
    window of the specified size and position
-   [newt\_pop\_help\_line](/ref/newt.html#newt_pop_help_line) —
    Replaces the current help line with the one from the stack
-   [newt\_pop\_window](/ref/newt.html#newt_pop_window) — Removes the
    top window from the display
-   [newt\_push\_help\_line](/ref/newt.html#newt_push_help_line) — Saves
    the current help line on a stack, and displays the new line
-   [newt\_radio\_get\_current](/ref/newt.html#newt_radio_get_current) —
    说明
-   [newt\_radiobutton](/ref/newt.html#newt_radiobutton) — 说明
-   [newt\_redraw\_help\_line](/ref/newt.html#newt_redraw_help_line) —
    说明
-   [newt\_reflow\_text](/ref/newt.html#newt_reflow_text) — 说明
-   [newt\_refresh](/ref/newt.html#newt_refresh) — Updates modified
    portions of the screen
-   [newt\_resize\_screen](/ref/newt.html#newt_resize_screen) — 说明
-   [newt\_resume](/ref/newt.html#newt_resume) — Resume using the newt
    interface after calling newt\_suspend
-   [newt\_run\_form](/ref/newt.html#newt_run_form) — Runs a form
-   [newt\_scale\_set](/ref/newt.html#newt_scale_set) — 说明
-   [newt\_scale](/ref/newt.html#newt_scale) — 说明
-   [newt\_scrollbar\_set](/ref/newt.html#newt_scrollbar_set) — 说明
-   [newt\_set\_help\_callback](/ref/newt.html#newt_set_help_callback) —
    说明
-   [newt\_set\_suspend\_callback](/ref/newt.html#newt_set_suspend_callback)
    — Set a callback function which gets invoked when user presses the
    suspend key
-   [newt\_suspend](/ref/newt.html#newt_suspend) — Tells newt to return
    the terminal to its initial state
-   [newt\_textbox\_get\_num\_lines](/ref/newt.html#newt_textbox_get_num_lines)
    — 说明
-   [newt\_textbox\_reflowed](/ref/newt.html#newt_textbox_reflowed) —
    说明
-   [newt\_textbox\_set\_height](/ref/newt.html#newt_textbox_set_height)
    — 说明
-   [newt\_textbox\_set\_text](/ref/newt.html#newt_textbox_set_text) —
    说明
-   [newt\_textbox](/ref/newt.html#newt_textbox) — 说明
-   [newt\_vertical\_scrollbar](/ref/newt.html#newt_vertical_scrollbar)
    — 说明
-   [newt\_wait\_for\_key](/ref/newt.html#newt_wait_for_key) — Doesn't
    return until a key has been pressed
-   [newt\_win\_choice](/ref/newt.html#newt_win_choice) — 说明
-   [newt\_win\_entries](/ref/newt.html#newt_win_entries) — 说明
-   [newt\_win\_menu](/ref/newt.html#newt_win_menu) — 说明
-   [newt\_win\_message](/ref/newt.html#newt_win_message) — 说明
-   [newt\_win\_messagev](/ref/newt.html#newt_win_messagev) — 说明
-   [newt\_win\_ternary](/ref/newt.html#newt_win_ternary) — 说明
