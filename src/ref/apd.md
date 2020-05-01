Contact information
-------------------

If you have comments, bugfixes, enhancements or want to help developing
this beast, you can send an mail to
<a href="mailto:apd@mail.communityconnect.com" class="link external">» apd@mail.communityconnect.com</a>.
Any help is very welcome.

apd\_breakpoint
===============

Stops the interpreter and waits on a CR from the socket

### 说明

<span class="type">bool</span> <span
class="methodname">apd\_breakpoint</span> ( <span
class="methodparam"><span class="type">int</span> `$debug_level`</span>
)

This can be used to stop the running of your script, and await responses
on the connected socket. To step the program, just send enter (a blank
line), or enter a php command to be executed.

### 参数

` debug_level`  
由加上 *XXX\_TRACE* 常量而形成的整数。

不建议使用 **`MEMORY_TRACE`**。这会很慢且似乎不精确。
**`ASSIGNMENT_TRACE`** 还未被实现。

要打开所有跟踪功能(TIMING, FUNCTIONS, ARGS SUMMARY (比如 strace -c))
则使用 99 作为值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Typical session using tcplisten**

``` shell
bash#tcplisten localhost 7777

APD - Advanced PHP Debugger Trace File
---------------------------------------------------------------------------
Process Pid (6118)
Trace Begun at Sun Mar 10 23:13:12 2002
---------------------------------------------------------------------------
(  0.000000): apd_set_session_trace called at /home/alan/Projects/project2/test. 
php:5
(  0.074824): apd_set_session_trace_socket() at /home/alan/Projects/project2/tes 
t.php:5 returned.  Elapsed (0.074824)
(  0.074918): apd_breakpoint() /home/alan/Projects/project2/test.php:7
              ++ argv[0] $(??) = 9
apd_breakpoint() at /home/alan/Projects/project2/test.php:7 returned.  Elapsed ( 
-2089521468.1073275368)
>\n 
statement: /home/alan/Projects/project2/test.php:8
>\n 
statement: /home/alan/Projects/project2/test.php:8
>\n 
statement: /home/alan/Projects/project2/test.php:10
>apd_echo($i);
EXEC: apd_echo($i);
0
>apd_echo(serialize(apd_get_active_symbols()));
EXEC:  apd_echo(serialize(apd_get_active_symbols()));
a:47:{i:0;s:4:"PWD";i:1;s:10:"COLORFGBG";i:2;s:11:"XAUTHORITY";i:3;s:14:"
COLORTERM_BCE";i:4;s:9:"WINDOWID";i:5;s:14:"ETERM_VERSION";i:6;s:16:"SE
SSION_MANAGER";i:7;s:4:"PS1";i:8;s:11:"GDMSESSION";i:9;s:5:"USER";i:10;s:5:"
MAIL";i:11;s:7:"OLDPWD";i:12;s:5:"LANG";i:13;s:10:"COLORTERM";i:14;s:8:"DISP
LAY";i:15;s:8:"LOGNAME";i:16;s:6:"
>apd_echo(system('ls /home/mydir'));
........
>apd_continue(0);
```

apd\_callstack
==============

Returns the current call stack as an array

### 说明

<span class="type">array</span> <span
class="methodname">apd\_callstack</span> ( <span
class="methodparam">void</span> )

Returns the current call stack as an array

### 返回值

An array containing the current call stack.

### 范例

**示例 \#1 <span class="function">apd\_callstack</span> example**

``` php
<?php
print_r(apd_callstack());
?>
```

apd\_clunk
==========

Throw a warning and a callstack

### 说明

<span class="type">void</span> <span
class="methodname">apd\_clunk</span> ( <span class="methodparam"><span
class="type">string</span> `$warning`</span> \[, <span
class="methodparam"><span class="type">string</span> `$delimiter`<span
class="initializer"> = "\<BR /\>"</span></span> \] )

Behaves like perl's *Carp::cluck*. Throw a warning and a callstack.

### 参数

`warning`  
The warning to throw.

`delimiter`  
The delimiter. Default to *\<BR /\>*.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">apd\_clunk</span> example**

``` php
<?php
apd_clunk("Some Warning", "<br/>");
?>
```

### 参见

-   <span class="function">apd\_croak</span>

apd\_continue
=============

Restarts the interpreter

### 说明

<span class="type">bool</span> <span
class="methodname">apd\_continue</span> ( <span
class="methodparam"><span class="type">int</span> `$debug_level`</span>
)

Usually sent via the socket to restart the interpreter.

### 参数

` debug_level`  
由加上 *XXX\_TRACE* 常量而形成的整数。

不建议使用 **`MEMORY_TRACE`**。这会很慢且似乎不精确。
**`ASSIGNMENT_TRACE`** 还未被实现。

要打开所有跟踪功能(TIMING, FUNCTIONS, ARGS SUMMARY (比如 strace -c))
则使用 99 作为值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">apd\_continue</span> example**

``` php
<?php
apd_continue(0);
?>
```

apd\_croak
==========

Throw an error, a callstack and then exit

### 说明

<span class="type">void</span> <span
class="methodname">apd\_croak</span> ( <span class="methodparam"><span
class="type">string</span> `$warning`</span> \[, <span
class="methodparam"><span class="type">string</span> `$delimiter`<span
class="initializer"> = "\<BR /\>"</span></span> \] )

Behaves like perl's *Carp::croak*. Throw an error, a callstack and then
exit.

### 参数

`warning`  
The warning to throw.

`delimiter`  
The delimiter. Default to *\<BR /\>*.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">apd\_croak</span> example**

``` php
<?php
apd_croak("Some Warning","<P>");
?>
```

### 参见

-   <span class="function">apd\_clunk</span>

apd\_dump\_function\_table
==========================

Outputs the current function table

### 说明

<span class="type">void</span> <span
class="methodname">apd\_dump\_function\_table</span> ( <span
class="methodparam">void</span> )

Outputs the current function table.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">apd\_dump\_function\_table</span>
example**

``` php
<?php
apd_dump_function_table();
?>
```

apd\_dump\_persistent\_resources
================================

Return all persistent resources as an array

### 说明

<span class="type">array</span> <span
class="methodname">apd\_dump\_persistent\_resources</span> ( <span
class="methodparam">void</span> )

Return all persistent resources as an array.

### 返回值

An array containing the current persistent resources.

### 范例

**示例 \#1 <span
class="function">apd\_dump\_persistent\_resources</span> example**

``` php
<?php
print_r(apd_dump_persistent_resources());
?>
```

### 参见

-   <span class="function">apd\_dump\_regular\_resources</span>

apd\_dump\_regular\_resources
=============================

Return all current regular resources as an array

### 说明

<span class="type">array</span> <span
class="methodname">apd\_dump\_regular\_resources</span> ( <span
class="methodparam">void</span> )

Return all current regular resources as an array.

### 返回值

An array containing the current regular resources.

### 范例

**示例 \#1 <span class="function">apd\_dump\_regular\_resources</span>
example**

``` php
<?php
print_r(apd_dump_regular_resources());
?>
```

### 参见

-   <span class="function">apd\_dump\_persistent\_resources</span>

apd\_echo
=========

Echo to the debugging socket

### 说明

<span class="type">bool</span> <span class="methodname">apd\_echo</span>
( <span class="methodparam"><span class="type">string</span>
`$output`</span> )

Usually sent via the socket to request information about the running
script.

### 参数

`output`  
The debugged variable.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">apd\_echo</span> example**

``` php
<?php
apd_echo($i);
?>
```

apd\_get\_active\_symbols
=========================

Get an array of the current variables names in the local scope

### 说明

<span class="type">array</span> <span
class="methodname">apd\_get\_active\_symbols</span> ( <span
class="methodparam">void</span> )

Returns the names of all the variables defined in the active scope, (not
their values).

### 返回值

A multidimensional array with all the variables.

### 范例

**示例 \#1 <span class="function">apd\_get\_active\_symbols</span>
example**

``` php
<?php
apd_echo(apd_get_active_symbols());
?>
```

apd\_set\_pprof\_trace
======================

Starts the session debugging

### 说明

<span class="type">string</span> <span
class="methodname">apd\_set\_pprof\_trace</span> (\[ <span
class="methodparam"><span class="type">string</span>
`$dump_directory`<span class="initializer"> =
ini\_get("apd.dumpdir")</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$fragment`<span
class="initializer"> = "pprof"</span></span> \]\] )

Starts debugging to `pprof_{process_id}` in the dump directory.

### 参数

`dump_directory`  
The directory in which the profile dump file is written. If not set, the
**apd.dumpdir** setting from the `php.ini` file is used.

`fragment`  

### 返回值

Returns path of the destination file.

### 范例

**示例 \#1 <span class="function">apd\_set\_pprof\_trace</span>
example**

``` php
<?php
apd_set_pprof_trace();
?>
```

### 参见

-   <span class="function">apd\_set\_session\_trace</span>

apd\_set\_session\_trace\_socket
================================

Starts the remote session debugging

### 说明

<span class="type">bool</span> <span
class="methodname">apd\_set\_session\_trace\_socket</span> ( <span
class="methodparam"><span class="type">string</span>
`$tcp_server`</span> , <span class="methodparam"><span
class="type">int</span> `$socket_type`</span> , <span
class="methodparam"><span class="type">int</span> `$port`</span> , <span
class="methodparam"><span class="type">int</span> `$debug_level`</span>
)

Connects to the specified `tcp_server` (eg. *tcplisten*) and sends
debugging data to the socket.

### 参数

`tcp_server`  
IP or Unix Domain socket (like a file) of the TCP server.

`socket_type`  
Can be **`AF_UNIX`** for file based sockets or **`APD_AF_INET`** for
standard tcp/ip.

`port`  
You can use any port, but higher numbers are better as most of the lower
numbers may be used by other system services.

` debug_level`  
由加上 *XXX\_TRACE* 常量而形成的整数。

不建议使用 **`MEMORY_TRACE`**。这会很慢且似乎不精确。
**`ASSIGNMENT_TRACE`** 还未被实现。

要打开所有跟踪功能(TIMING, FUNCTIONS, ARGS SUMMARY (比如 strace -c))
则使用 99 作为值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span
class="function">apd\_set\_session\_trace\_socket</span> example**

``` php
<?php
  apd_set_session_trace_socket("127.0.0.1",APD_AF_INET,7112,0);
?>
```

apd\_set\_session\_trace
========================

Starts the session debugging

### 说明

<span class="type">void</span> <span
class="methodname">apd\_set\_session\_trace</span> ( <span
class="methodparam"><span class="type">int</span> `$debug_level`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$dump_directory`<span class="initializer"> =
ini\_get("apd.dumpdir")</span></span> \] )

Starts debugging to `apd_dump_{process_id}` in the dump directory.

### 参数

` debug_level`  
由加上 *XXX\_TRACE* 常量而形成的整数。

不建议使用 **`MEMORY_TRACE`**。这会很慢且似乎不精确。
**`ASSIGNMENT_TRACE`** 还未被实现。

要打开所有跟踪功能(TIMING, FUNCTIONS, ARGS SUMMARY (比如 strace -c))
则使用 99 作为值。

`dump_directory`  
The directory in which the profile dump file is written. If not set, the
*apd.dumpdir* setting from the `php.ini` file is used.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">apd\_set\_session\_trace</span>
example**

``` php
<?php
apd_set_session_trace(99);
?>
```

apd\_set\_session
=================

Changes or sets the current debugging level

### 说明

<span class="type">void</span> <span
class="methodname">apd\_set\_session</span> ( <span
class="methodparam"><span class="type">int</span> `$debug_level`</span>
)

This can be used to increase or decrease debugging in a different area
of your application.

### 参数

` debug_level`  
由加上 *XXX\_TRACE* 常量而形成的整数。

不建议使用 **`MEMORY_TRACE`**。这会很慢且似乎不精确。
**`ASSIGNMENT_TRACE`** 还未被实现。

要打开所有跟踪功能(TIMING, FUNCTIONS, ARGS SUMMARY (比如 strace -c))
则使用 99 作为值。

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">apd\_set\_session</span> example**

``` php
<?php
apd_set_session(9);
?>
```

override\_function
==================

Overrides built-in functions

### 说明

<span class="type">bool</span> <span
class="methodname">override\_function</span> ( <span
class="methodparam"><span class="type">string</span>
`$function_name`</span> , <span class="methodparam"><span
class="type">string</span> `$function_args`</span> , <span
class="methodparam"><span class="type">string</span>
`$function_code`</span> )

Overrides built-in functions by replacing them in the symbol table.

### 参数

`function_name`  
The function to override.

`function_args`  
The function arguments, as a comma separated string.

Usually you will want to pass this parameter, as well as the
`function_code` parameter, as a single quote delimited string. The
reason for using single quoted strings, is to protect the variable names
from parsing, otherwise, if you use double quotes there will be a need
to escape the variable names, e.g. \\`$your_var`.

`function_code`  
The new code for the function.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">override\_function</span> example**

``` php
<?php
override_function('test', '$a,$b', 'echo "DOING TEST"; return $a * $b;');
?>
```

rename\_function
================

Renames orig\_name to new\_name in the global function table

### 说明

<span class="type">bool</span> <span
class="methodname">rename\_function</span> ( <span
class="methodparam"><span class="type">string</span>
`$original_name`</span> , <span class="methodparam"><span
class="type">string</span> `$new_name`</span> )

Renames a orig\_name to new\_name in the global function table. Useful
for temporarily overriding built-in functions.

### 参数

`original_name`  
The original function name.

`new_name`  
The new name for the `original_name` function.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">rename\_function</span> example**

``` php
<?php
rename_function('mysql_connect', 'debug_mysql_connect' );
?>
```

**目录**

-   [apd\_breakpoint](/ref/apd.html#apd_breakpoint) — Stops the
    interpreter and waits on a CR from the socket
-   [apd\_callstack](/ref/apd.html#apd_callstack) — Returns the current
    call stack as an array
-   [apd\_clunk](/ref/apd.html#apd_clunk) — Throw a warning and a
    callstack
-   [apd\_continue](/ref/apd.html#apd_continue) — Restarts the
    interpreter
-   [apd\_croak](/ref/apd.html#apd_croak) — Throw an error, a callstack
    and then exit
-   [apd\_dump\_function\_table](/ref/apd.html#apd_dump_function_table)
    — Outputs the current function table
-   [apd\_dump\_persistent\_resources](/ref/apd.html#apd_dump_persistent_resources)
    — Return all persistent resources as an array
-   [apd\_dump\_regular\_resources](/ref/apd.html#apd_dump_regular_resources)
    — Return all current regular resources as an array
-   [apd\_echo](/ref/apd.html#apd_echo) — Echo to the debugging socket
-   [apd\_get\_active\_symbols](/ref/apd.html#apd_get_active_symbols) —
    Get an array of the current variables names in the local scope
-   [apd\_set\_pprof\_trace](/ref/apd.html#apd_set_pprof_trace) — Starts
    the session debugging
-   [apd\_set\_session\_trace\_socket](/ref/apd.html#apd_set_session_trace_socket)
    — Starts the remote session debugging
-   [apd\_set\_session\_trace](/ref/apd.html#apd_set_session_trace) —
    Starts the session debugging
-   [apd\_set\_session](/ref/apd.html#apd_set_session) — Changes or sets
    the current debugging level
-   [override\_function](/ref/apd.html#override_function) — Overrides
    built-in functions
-   [rename\_function](/ref/apd.html#rename_function) — Renames
    orig\_name to new\_name in the global function table
