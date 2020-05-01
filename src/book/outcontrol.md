输出缓冲控制
============

**目录**

-   [简介](/intro/outcontrol.html)
-   [安装／配置](/outcontrol/setup.html)
    -   [需求](/outcontrol/setup.html#需求)
    -   [安装](/outcontrol/setup.html#安装)
    -   [运行时配置](/outcontrol/setup.html#运行时配置)
    -   [资源类型](/outcontrol/setup.html#资源类型)
-   [预定义常量](/outcontrol/constants.html)
-   [范例](/outcontrol/examples.html)
    -   [基本用法](/outcontrol/examples.html#基本用法)
-   [Output Control 函数](/ref/outcontrol.html)
    -   [flush](/ref/outcontrol.html#flush) — 刷新输出缓冲
    -   [ob\_clean](/ref/outcontrol.html#ob_clean) —
        清空（擦掉）输出缓冲区
    -   [ob\_end\_clean](/ref/outcontrol.html#ob_end_clean) —
        清空（擦除）缓冲区并关闭输出缓冲
    -   [ob\_end\_flush](/ref/outcontrol.html#ob_end_flush) —
        冲刷出（送出）输出缓冲区内容并关闭缓冲
    -   [ob\_flush](/ref/outcontrol.html#ob_flush) —
        冲刷出（送出）输出缓冲区中的内容
    -   [ob\_get\_clean](/ref/outcontrol.html#ob_get_clean) —
        得到当前缓冲区的内容并删除当前输出缓。
    -   [ob\_get\_contents](/ref/outcontrol.html#ob_get_contents) —
        返回输出缓冲区的内容
    -   [ob\_get\_flush](/ref/outcontrol.html#ob_get_flush) —
        刷出（送出）缓冲区内容，以字符串形式返回内容，并关闭输出缓冲区。
    -   [ob\_get\_length](/ref/outcontrol.html#ob_get_length) —
        返回输出缓冲区内容的长度
    -   [ob\_get\_level](/ref/outcontrol.html#ob_get_level) —
        返回输出缓冲机制的嵌套级别
    -   [ob\_get\_status](/ref/outcontrol.html#ob_get_status) —
        得到所有输出缓冲区的状态
    -   [ob\_gzhandler](/ref/outcontrol.html#ob_gzhandler) —
        在ob\_start中使用的用来压缩输出缓冲区中内容的回调函数。ob\_start
        callback function to gzip output buffer
    -   [ob\_implicit\_flush](/ref/outcontrol.html#ob_implicit_flush) —
        打开/关闭绝对刷送
    -   [ob\_list\_handlers](/ref/outcontrol.html#ob_list_handlers) —
        列出所有使用中的输出处理程序。
    -   [ob\_start](/ref/outcontrol.html#ob_start) — 打开输出控制缓冲
    -   [output\_add\_rewrite\_var](/ref/outcontrol.html#output_add_rewrite_var)
        — 添加URL重写器的值（Add URL rewriter values）
    -   [output\_reset\_rewrite\_vars](/ref/outcontrol.html#output_reset_rewrite_vars)
        — 重设URL重写器的值（Reset URL rewriter values）
