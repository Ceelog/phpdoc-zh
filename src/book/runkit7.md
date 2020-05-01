runkit7
=======

**目录**

-   [简介](/intro/runkit7.html)
-   [安装／配置](/runkit7/setup.html)
    -   [需求](/runkit7/setup.html#需求)
    -   [安装](/runkit7/setup.html#安装)
    -   [运行时配置](/runkit7/setup.html#运行时配置)
    -   [资源类型](/runkit7/setup.html#资源类型)
-   [预定义常量](/runkit7/constants.html)
-   [runkit7 函数](/ref/runkit7.html)
    -   [runkit7\_constant\_add](/ref/runkit7.html#runkit7_constant_add)
        — Similar to define(), but allows defining in class definitions
        as well
    -   [runkit7\_constant\_redefine](/ref/runkit7.html#runkit7_constant_redefine)
        — Redefine an already defined constant
    -   [runkit7\_constant\_remove](/ref/runkit7.html#runkit7_constant_remove)
        — Remove/Delete an already defined constant
    -   [runkit7\_function\_add](/ref/runkit7.html#runkit7_function_add)
        — Add a new function, similar to create\_function
    -   [runkit7\_function\_copy](/ref/runkit7.html#runkit7_function_copy)
        — Copy a function to a new function name
    -   [runkit7\_function\_redefine](/ref/runkit7.html#runkit7_function_redefine)
        — Replace a function definition with a new implementation
    -   [runkit7\_function\_remove](/ref/runkit7.html#runkit7_function_remove)
        — Remove a function definition
    -   [runkit7\_function\_rename](/ref/runkit7.html#runkit7_function_rename)
        — Change a function's name
    -   [runkit7\_import](/ref/runkit7.html#runkit7_import) — Process a
        PHP file importing function and class definitions, overwriting
        where appropriate
    -   [runkit7\_method\_add](/ref/runkit7.html#runkit7_method_add) —
        Dynamically adds a new method to a given class
    -   [runkit7\_method\_copy](/ref/runkit7.html#runkit7_method_copy) —
        Copies a method from class to another
    -   [runkit7\_method\_redefine](/ref/runkit7.html#runkit7_method_redefine)
        — Dynamically changes the code of the given method
    -   [runkit7\_method\_remove](/ref/runkit7.html#runkit7_method_remove)
        — Dynamically removes the given method
    -   [runkit7\_method\_rename](/ref/runkit7.html#runkit7_method_rename)
        — Dynamically changes the name of the given method
    -   [runkit7\_object\_id](/ref/runkit7.html#runkit7_object_id) —
        Return the integer object handle for given object
    -   [runkit7\_superglobals](/ref/runkit7.html#runkit7_superglobals)
        — Return numerically indexed array of registered superglobals
    -   [runkit7\_zval\_inspect](/ref/runkit7.html#runkit7_zval_inspect)
        — Returns information about the passed in value with data types,
        reference counts, etc
