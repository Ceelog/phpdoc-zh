系统程序执行
============

**目录**

-   [简介](/intro/exec.html)
-   [安装／配置](/exec/setup.html)
    -   [需求](/exec/setup.html#需求)
    -   [安装](/exec/setup.html#安装)
    -   [运行时配置](/exec/setup.html#运行时配置)
    -   [资源类型](/exec/setup.html#资源类型)
-   [预定义常量](/exec/constants.html)
-   [程序执行函数](/ref/exec.html)
    -   [escapeshellarg](/ref/exec.html#escapeshellarg) —
        把字符串转码为可以在 shell 命令里使用的参数
    -   [escapeshellcmd](/ref/exec.html#escapeshellcmd) — shell
        元字符转义
    -   [exec](/ref/exec.html#exec) — 执行一个外部程序
    -   [passthru](/ref/exec.html#passthru) —
        执行外部程序并且显示原始输出
    -   [proc\_close](/ref/exec.html#proc_close) — 关闭由 proc\_open
        打开的进程并且返回进程退出码
    -   [proc\_get\_status](/ref/exec.html#proc_get_status) — 获取由
        proc\_open 函数打开的进程的信息
    -   [proc\_nice](/ref/exec.html#proc_nice) — 修改当前进程的优先级
    -   [proc\_open](/ref/exec.html#proc_open) —
        执行一个命令，并且打开用来输入/输出的文件指针。
    -   [proc\_terminate](/ref/exec.html#proc_terminate) — 杀除由
        proc\_open 打开的进程
    -   [shell\_exec](/ref/exec.html#shell_exec) — 通过 shell
        环境执行命令，并且将完整的输出以字符串的方式返回。
    -   [system](/ref/exec.html#system) — 执行外部程序，并且显示输出
