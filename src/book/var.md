Variable handling
=================

**目录**

-   [简介](/intro/var.html)
-   [安装／配置](/var/setup.html)
    -   [需求](/var/setup.html#需求)
    -   [安装](/var/setup.html#安装)
    -   [运行时配置](/var/setup.html#运行时配置)
    -   [资源类型](/var/setup.html#资源类型)
-   [预定义常量](/var/constants.html)
-   [Variable handling 函数](/ref/var.html)
    -   [boolval](/ref/var.html#boolval) — 获取变量的布尔值
    -   [debug\_zval\_dump](/ref/var.html#debug_zval_dump) — Dumps a
        string representation of an internal zend value to output
    -   [doubleval](/ref/var.html#doubleval) — floatval 的别名
    -   [empty](/ref/var.html#empty) — 检查一个变量是否为空
    -   [floatval](/ref/var.html#floatval) — 获取变量的浮点值
    -   [get\_defined\_vars](/ref/var.html#get_defined_vars) —
        返回由所有已定义变量所组成的数组
    -   [get\_resource\_type](/ref/var.html#get_resource_type) —
        返回资源（resource）类型
    -   [gettype](/ref/var.html#gettype) — 获取变量的类型
    -   [intval](/ref/var.html#intval) — 获取变量的整数值
    -   [is\_array](/ref/var.html#is_array) — 检测变量是否是数组
    -   [is\_bool](/ref/var.html#is_bool) — 检测变量是否是布尔型
    -   [is\_callable](/ref/var.html#is_callable) —
        检测参数是否为合法的可调用结构
    -   [is\_countable](/ref/var.html#is_countable) — Verify that the
        contents of a variable is a countable value
    -   [is\_double](/ref/var.html#is_double) — is\_float 的别名
    -   [is\_float](/ref/var.html#is_float) — 检测变量是否是浮点型
    -   [is\_int](/ref/var.html#is_int) — 检测变量是否是整数
    -   [is\_integer](/ref/var.html#is_integer) — is\_int 的别名
    -   [is\_iterable](/ref/var.html#is_iterable) — Verify that the
        contents of a variable is an iterable value
    -   [is\_long](/ref/var.html#is_long) — is\_int 的别名
    -   [is\_null](/ref/var.html#is_null) — 检测变量是否为 NULL
    -   [is\_numeric](/ref/var.html#is_numeric) —
        检测变量是否为数字或数字字符串
    -   [is\_object](/ref/var.html#is_object) — 检测变量是否是一个对象
    -   [is\_real](/ref/var.html#is_real) — is\_float 的别名
    -   [is\_resource](/ref/var.html#is_resource) —
        检测变量是否为资源类型
    -   [is\_scalar](/ref/var.html#is_scalar) — 检测变量是否是一个标量
    -   [is\_string](/ref/var.html#is_string) — 检测变量是否是字符串
    -   [isset](/ref/var.html#isset) — 检测变量是否已设置并且非 NULL
    -   [print\_r](/ref/var.html#print_r) — 以易于理解的格式打印变量。
    -   [serialize](/ref/var.html#serialize) — 产生一个可存储的值的表示
    -   [settype](/ref/var.html#settype) — 设置变量的类型
    -   [strval](/ref/var.html#strval) — 获取变量的字符串值
    -   [unserialize](/ref/var.html#unserialize) — 从已存储的表示中创建
        PHP 的值
    -   [unset](/ref/var.html#unset) — 释放给定的变量
    -   [var\_dump](/ref/var.html#var_dump) — 打印变量的相关信息
    -   [var\_export](/ref/var.html#var_export) —
        输出或返回一个变量的字符串表示
