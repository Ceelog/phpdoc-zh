runkit
======

**目录**

-   [简介](/intro/runkit.html)
-   [预定义常量](/runkit/constants.html)
-   [安装／配置](/runkit/setup.html)
    -   [需求](/runkit/setup.html#需求)
    -   [安装](/runkit/setup.html#安装)
    -   [运行时配置](/runkit/setup.html#运行时配置)
    -   [资源类型](/runkit/setup.html#资源类型)
-   [runkit 函数](/ref/runkit.html)
    -   [Runkit\_Sandbox](/ref/runkit.html#Runkit_Sandbox) — Runkit
        Sandbox Class -- PHP Virtual Machine
    -   [Runkit\_Sandbox\_Parent](/ref/runkit.html#Runkit_Sandbox_Parent)
        — Runkit Anti-Sandbox Class
    -   [runkit\_class\_adopt](/ref/runkit.html#runkit_class_adopt) —
        Convert a base class to an inherited class, add ancestral
        methods when appropriate
    -   [runkit\_class\_emancipate](/ref/runkit.html#runkit_class_emancipate)
        — Convert an inherited class to a base class, removes any method
        whose scope is ancestral
    -   [runkit\_constant\_add](/ref/runkit.html#runkit_constant_add) —
        Similar to define(), but allows defining in class definitions as
        well
    -   [runkit\_constant\_redefine](/ref/runkit.html#runkit_constant_redefine)
        — Redefine an already defined constant
    -   [runkit\_constant\_remove](/ref/runkit.html#runkit_constant_remove)
        — Remove/Delete an already defined constant
    -   [runkit\_function\_add](/ref/runkit.html#runkit_function_add) —
        Add a new function, similar to create\_function
    -   [runkit\_function\_copy](/ref/runkit.html#runkit_function_copy)
        — Copy a function to a new function name
    -   [runkit\_function\_redefine](/ref/runkit.html#runkit_function_redefine)
        — Replace a function definition with a new implementation
    -   [runkit\_function\_remove](/ref/runkit.html#runkit_function_remove)
        — Remove a function definition
    -   [runkit\_function\_rename](/ref/runkit.html#runkit_function_rename)
        — Change a function's name
    -   [runkit\_import](/ref/runkit.html#runkit_import) — Process a PHP
        file importing function and class definitions, overwriting where
        appropriate
    -   [runkit\_lint\_file](/ref/runkit.html#runkit_lint_file) — Check
        the PHP syntax of the specified file
    -   [runkit\_lint](/ref/runkit.html#runkit_lint) — Check the PHP
        syntax of the specified php code
    -   [runkit\_method\_add](/ref/runkit.html#runkit_method_add) —
        Dynamically adds a new method to a given class
    -   [runkit\_method\_copy](/ref/runkit.html#runkit_method_copy) —
        Copies a method from class to another
    -   [runkit\_method\_redefine](/ref/runkit.html#runkit_method_redefine)
        — Dynamically changes the code of the given method
    -   [runkit\_method\_remove](/ref/runkit.html#runkit_method_remove)
        — Dynamically removes the given method
    -   [runkit\_method\_rename](/ref/runkit.html#runkit_method_rename)
        — Dynamically changes the name of the given method
    -   [runkit\_return\_value\_used](/ref/runkit.html#runkit_return_value_used)
        — Determines if the current functions return value will be used
    -   [runkit\_sandbox\_output\_handler](/ref/runkit.html#runkit_sandbox_output_handler)
        — Specify a function to capture and/or process output from a
        runkit sandbox
    -   [runkit\_superglobals](/ref/runkit.html#runkit_superglobals) —
        Return numerically indexed array of registered superglobals
