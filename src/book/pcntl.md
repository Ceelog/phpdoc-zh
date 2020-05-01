进程控制
========

**目录**

-   [简介](/intro/pcntl.html)
-   [安装／配置](/pcntl/setup.html)
    -   [需求](/pcntl/setup.html#需求)
    -   [安装](/pcntl/setup.html#安装)
    -   [运行时配置](/pcntl/setup.html#运行时配置)
    -   [资源类型](/pcntl/setup.html#资源类型)
-   [预定义常量](/pcntl/constants.html)
-   [范例](/pcntl/examples.html)
    -   [](/pcntl/examples.html#)
-   [PCNTL 函数](/ref/pcntl.html)
    -   [pcntl\_alarm](/ref/pcntl.html#pcntl_alarm) —
        为进程设置一个alarm闹钟信号
    -   [pcntl\_async\_signals](/ref/pcntl.html#pcntl_async_signals) —
        Enable/disable asynchronous signal handling or return the old
        setting
    -   [pcntl\_errno](/ref/pcntl.html#pcntl_errno) — 别名
        pcntl\_get\_last\_error
    -   [pcntl\_exec](/ref/pcntl.html#pcntl_exec) —
        在当前进程空间执行指定程序
    -   [pcntl\_fork](/ref/pcntl.html#pcntl_fork) —
        在当前进程当前位置产生分支（子进程）。译注：fork是创建了一个子进程，父进程和子进程
        都从fork的位置开始向下继续执行，不同的是父进程执行过程中，得到的fork返回值为子进程
        号，而子进程得到的是0。
    -   [pcntl\_get\_last\_error](/ref/pcntl.html#pcntl_get_last_error)
        — Retrieve the error number set by the last pcntl function which
        failed
    -   [pcntl\_getpriority](/ref/pcntl.html#pcntl_getpriority) —
        获取任意进程的优先级
    -   [pcntl\_setpriority](/ref/pcntl.html#pcntl_setpriority) —
        修改任意进程的优先级
    -   [pcntl\_signal\_dispatch](/ref/pcntl.html#pcntl_signal_dispatch)
        — 调用等待信号的处理器
    -   [pcntl\_signal\_get\_handler](/ref/pcntl.html#pcntl_signal_get_handler)
        — Get the current handler for specified signal
    -   [pcntl\_signal](/ref/pcntl.html#pcntl_signal) —
        安装一个信号处理器
    -   [pcntl\_sigprocmask](/ref/pcntl.html#pcntl_sigprocmask) —
        设置或检索阻塞信号
    -   [pcntl\_sigtimedwait](/ref/pcntl.html#pcntl_sigtimedwait) —
        带超时机制的信号等待
    -   [pcntl\_sigwaitinfo](/ref/pcntl.html#pcntl_sigwaitinfo) —
        等待信号
    -   [pcntl\_strerror](/ref/pcntl.html#pcntl_strerror) — Retrieve the
        system error message associated with the given errno
    -   [pcntl\_wait](/ref/pcntl.html#pcntl_wait) —
        等待或返回fork的子进程状态
    -   [pcntl\_waitpid](/ref/pcntl.html#pcntl_waitpid) —
        等待或返回fork的子进程状态
    -   [pcntl\_wexitstatus](/ref/pcntl.html#pcntl_wexitstatus) —
        返回一个中断的子进程的返回代码
    -   [pcntl\_wifexited](/ref/pcntl.html#pcntl_wifexited) —
        检查状态代码是否代表一个正常的退出。
    -   [pcntl\_wifsignaled](/ref/pcntl.html#pcntl_wifsignaled) —
        检查子进程状态码是否代表由于某个信号而中断
    -   [pcntl\_wifstopped](/ref/pcntl.html#pcntl_wifstopped) —
        检查子进程当前是否已经停止
    -   [pcntl\_wstopsig](/ref/pcntl.html#pcntl_wstopsig) —
        返回导致子进程停止的信号
    -   [pcntl\_wtermsig](/ref/pcntl.html#pcntl_wtermsig) —
        返回导致子进程中断的信号
