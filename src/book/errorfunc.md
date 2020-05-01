错误处理和日志记录
==================

**目录**

-   [简介](/intro/errorfunc.html)
-   [安装／配置](/errorfunc/setup.html)
    -   [需求](/errorfunc/setup.html#需求)
    -   [安装](/errorfunc/setup.html#安装)
    -   [运行时配置](/errorfunc/setup.html#运行时配置)
    -   [资源类型](/errorfunc/setup.html#资源类型)
-   [预定义常量](/errorfunc/constants.html)
-   [范例](/errorfunc/examples.html)
-   [错误处理 函数](/ref/errorfunc.html)
    -   [debug\_backtrace](/ref/errorfunc.html#debug_backtrace) —
        产生一条回溯跟踪(backtrace)
    -   [debug\_print\_backtrace](/ref/errorfunc.html#debug_print_backtrace)
        — 打印一条回溯。
    -   [error\_clear\_last](/ref/errorfunc.html#error_clear_last) —
        清除最近一次错误
    -   [error\_get\_last](/ref/errorfunc.html#error_get_last) —
        获取最后发生的错误
    -   [error\_log](/ref/errorfunc.html#error_log) —
        发送错误信息到某个地方
    -   [error\_reporting](/ref/errorfunc.html#error_reporting) —
        设置应该报告何种 PHP 错误
    -   [restore\_error\_handler](/ref/errorfunc.html#restore_error_handler)
        — 还原之前的错误处理函数
    -   [restore\_exception\_handler](/ref/errorfunc.html#restore_exception_handler)
        — 恢复之前定义过的异常处理函数。
    -   [set\_error\_handler](/ref/errorfunc.html#set_error_handler) —
        设置用户自定义的错误处理函数
    -   [set\_exception\_handler](/ref/errorfunc.html#set_exception_handler)
        — 设置用户自定义的异常处理函数
    -   [trigger\_error](/ref/errorfunc.html#trigger_error) —
        产生一个用户级别的 error/warning/notice 信息
    -   [user\_error](/ref/errorfunc.html#user_error) — trigger\_error
        的别名
