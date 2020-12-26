phpdbg\_break\_file
===================

Inserts a breakpoint at a line in a file

### 说明

<span class="type">void</span> <span
class="methodname">phpdbg\_break\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> ,
<span class="methodparam"><span class="type">int</span> `$line`</span> )

Insert a breakpoint at the given `line` in the given `file`.

### 参数

`file`  
The name of the file.

`line`  
The line number.

### 返回值

没有返回值。

### 参见

-   <span class="function">phpdbg\_break\_function</span>
-   <span class="function">phpdbg\_break\_method</span>
-   <span class="function">phpdbg\_break\_next</span>
-   <span class="function">phpdbg\_clear</span>

phpdbg\_break\_function
=======================

Inserts a breakpoint at entry to a function

### 说明

<span class="type">void</span> <span
class="methodname">phpdbg\_break\_function</span> ( <span
class="methodparam"><span class="type">string</span> `$function`</span>
)

Insert a breakpoint at the entry to the given `function`.

### 参数

`function`  
The name of the function.

### 返回值

没有返回值。

### 参见

-   <span class="function">phpdbg\_break\_file</span>
-   <span class="function">phpdbg\_break\_method</span>
-   <span class="function">phpdbg\_break\_next</span>
-   <span class="function">phpdbg\_clear</span>

phpdbg\_break\_method
=====================

Inserts a breakpoint at entry to a method

### 说明

<span class="type">void</span> <span
class="methodname">phpdbg\_break\_method</span> ( <span
class="methodparam"><span class="type">string</span> `$class`</span> ,
<span class="methodparam"><span class="type">string</span>
`$method`</span> )

Insert a breakpoint at the entry to the given `method` of the given
`class`.

### 参数

`class`  
The name of the class.

`method`  
The name of the method.

### 返回值

没有返回值。

### 参见

-   <span class="function">phpdbg\_break\_file</span>
-   <span class="function">phpdbg\_break\_function</span>
-   <span class="function">phpdbg\_break\_next</span>
-   <span class="function">phpdbg\_clear</span>

phpdbg\_break\_next
===================

Inserts a breakpoint at the next opcode

### 说明

<span class="type">void</span> <span
class="methodname">phpdbg\_break\_next</span> ( <span
class="methodparam">void</span> )

Insert a breakpoint at the next opcode.

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="function">phpdbg\_break\_file</span>
-   <span class="function">phpdbg\_break\_function</span>
-   <span class="function">phpdbg\_break\_method</span>
-   <span class="function">phpdbg\_clear</span>

phpdbg\_clear
=============

Clears all breakpoints

### 说明

<span class="type">void</span> <span
class="methodname">phpdbg\_clear</span> ( <span
class="methodparam">void</span> )

Clear all breakpoints that have been set, either via one of the <span
class="function">phpdbg\_break\_\*</span> functions or interactively in
the console.

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

### 参见

-   <span class="function">phpdbg\_break\_file</span>
-   <span class="function">phpdbg\_break\_function</span>
-   <span class="function">phpdbg\_break\_method</span>
-   <span class="function">phpdbg\_break\_next</span>

phpdbg\_color
=============

Sets the color of certain elements

### 说明

<span class="type">void</span> <span
class="methodname">phpdbg\_color</span> ( <span
class="methodparam"><span class="type">int</span> `$element`</span> ,
<span class="methodparam"><span class="type">string</span>
`$color`</span> )

Set the `color` of the given `element`.

### 参数

`element`  
One of the **`PHPDBG_COLOR_*`** constants.

`color`  
The name of the color. One of *white*, *red*, *green*, *yellow*, *blue*,
*purple*, *cyan* or *black*, optionally with either a trailing *-bold*
or *-underline*, for instance, *white-bold* or *green-underline*.

### 返回值

没有返回值。

### 参见

-   <span class="function">phpdbg\_prompt</span>

phpdbg\_end\_oplog
==================

### 说明

<span class="type"><span class="type">array</span><span
class="type">null</span></span> <span
class="methodname">phpdbg\_end\_oplog</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = \[\]</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`options`  

### 返回值

phpdbg\_exec
============

Attempts to set the execution context

### 说明

<span class="type"><span class="type">string</span><span
class="type">bool</span></span> <span
class="methodname">phpdbg\_exec</span> ( <span class="methodparam"><span
class="type">string</span> `$context`</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`context`  

### 返回值

If the execution context was set previously it is returned. If the
execution context was not set previously **`true`** is returned. If the
request to set the context fails, **`false`** is returned, and an
**`E_WARNING`** raised.

phpdbg\_get\_executable
=======================

### 说明

<span class="type">array</span> <span
class="methodname">phpdbg\_get\_executable</span> (\[ <span
class="methodparam"><span class="type">array</span> `$options`<span
class="initializer"> = \[\]</span></span> \] )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

`options`  

### 返回值

phpdbg\_prompt
==============

Sets the command prompt

### 说明

<span class="type">void</span> <span
class="methodname">phpdbg\_prompt</span> ( <span
class="methodparam"><span class="type">string</span> `$string`</span> )

Set the command prompt to the given `string`.

### 参数

`string`  
The string to use as command prompt.

### 返回值

没有返回值。

### 参见

-   <span class="function">phpdbg\_color</span>

phpdbg\_start\_oplog
====================

### 说明

<span class="type">void</span> <span
class="methodname">phpdbg\_start\_oplog</span> ( <span
class="methodparam">void</span> )

**Warning**

本函数还未编写文档，仅有参数列表。

### 参数

此函数没有参数。

### 返回值

没有返回值。

**目录**

-   [phpdbg\_break\_file](/ref/phpdbg.html#phpdbg_break_file) — Inserts
    a breakpoint at a line in a file
-   [phpdbg\_break\_function](/ref/phpdbg.html#phpdbg_break_function) —
    Inserts a breakpoint at entry to a function
-   [phpdbg\_break\_method](/ref/phpdbg.html#phpdbg_break_method) —
    Inserts a breakpoint at entry to a method
-   [phpdbg\_break\_next](/ref/phpdbg.html#phpdbg_break_next) — Inserts
    a breakpoint at the next opcode
-   [phpdbg\_clear](/ref/phpdbg.html#phpdbg_clear) — Clears all
    breakpoints
-   [phpdbg\_color](/ref/phpdbg.html#phpdbg_color) — Sets the color of
    certain elements
-   [phpdbg\_end\_oplog](/ref/phpdbg.html#phpdbg_end_oplog) — 说明
-   [phpdbg\_exec](/ref/phpdbg.html#phpdbg_exec) — Attempts to set the
    execution context
-   [phpdbg\_get\_executable](/ref/phpdbg.html#phpdbg_get_executable) —
    说明
-   [phpdbg\_prompt](/ref/phpdbg.html#phpdbg_prompt) — Sets the command
    prompt
-   [phpdbg\_start\_oplog](/ref/phpdbg.html#phpdbg_start_oplog) — 说明
