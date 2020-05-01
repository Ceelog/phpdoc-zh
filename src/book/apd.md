Advanced PHP debugger
=====================

**目录**

-   [简介](/intro/apd.html)
-   [安装／配置](/apd/setup.html)
    -   [需求](/apd/setup.html#需求)
    -   [安装](/apd/setup.html#安装)
    -   [Building on Win32](/apd/setup.html#Building%20on%20Win32)
    -   [运行时配置](/apd/setup.html#运行时配置)
    -   [资源类型](/apd/setup.html#资源类型)
-   [预定义常量](/apd/constants.html)
-   [范例](/apd/examples.html)
    -   [How to use PHP-APD in your
        scripts](/apd/examples.html#How%20to%20use%20PHP-APD%20in%20your%20scripts)
-   [APD 函数](/ref/apd.html)
    -   [apd\_breakpoint](/ref/apd.html#apd_breakpoint) — Stops the
        interpreter and waits on a CR from the socket
    -   [apd\_callstack](/ref/apd.html#apd_callstack) — Returns the
        current call stack as an array
    -   [apd\_clunk](/ref/apd.html#apd_clunk) — Throw a warning and a
        callstack
    -   [apd\_continue](/ref/apd.html#apd_continue) — Restarts the
        interpreter
    -   [apd\_croak](/ref/apd.html#apd_croak) — Throw an error, a
        callstack and then exit
    -   [apd\_dump\_function\_table](/ref/apd.html#apd_dump_function_table)
        — Outputs the current function table
    -   [apd\_dump\_persistent\_resources](/ref/apd.html#apd_dump_persistent_resources)
        — Return all persistent resources as an array
    -   [apd\_dump\_regular\_resources](/ref/apd.html#apd_dump_regular_resources)
        — Return all current regular resources as an array
    -   [apd\_echo](/ref/apd.html#apd_echo) — Echo to the debugging
        socket
    -   [apd\_get\_active\_symbols](/ref/apd.html#apd_get_active_symbols)
        — Get an array of the current variables names in the local scope
    -   [apd\_set\_pprof\_trace](/ref/apd.html#apd_set_pprof_trace) —
        Starts the session debugging
    -   [apd\_set\_session\_trace\_socket](/ref/apd.html#apd_set_session_trace_socket)
        — Starts the remote session debugging
    -   [apd\_set\_session\_trace](/ref/apd.html#apd_set_session_trace)
        — Starts the session debugging
    -   [apd\_set\_session](/ref/apd.html#apd_set_session) — Changes or
        sets the current debugging level
    -   [override\_function](/ref/apd.html#override_function) —
        Overrides built-in functions
    -   [rename\_function](/ref/apd.html#rename_function) — Renames
        orig\_name to new\_name in the global function table
