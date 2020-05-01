GNU Readline
============

**目录**

-   [简介](/intro/readline.html)
-   [安装／配置](/readline/setup.html)
    -   [需求](/readline/setup.html#需求)
    -   [安装](/readline/setup.html#安装)
    -   [运行时配置](/readline/setup.html#运行时配置)
    -   [资源类型](/readline/setup.html#资源类型)
-   [预定义常量](/readline/constants.html)
-   [Readline 函数](/ref/readline.html)
    -   [readline\_add\_history](/ref/readline.html#readline_add_history)
        — 添加一行命令行历史记录
    -   [readline\_callback\_handler\_install](/ref/readline.html#readline_callback_handler_install)
        — 初始化一个 readline 回调接口，然后终端输出提示信息并立即返回
    -   [readline\_callback\_handler\_remove](/ref/readline.html#readline_callback_handler_remove)
        — 移除上一个安装的回调函数句柄并且恢复终端设置
    -   [readline\_callback\_read\_char](/ref/readline.html#readline_callback_read_char)
        — 当一个行被接收时读取一个字符并且通知 readline 调用回调函数
    -   [readline\_clear\_history](/ref/readline.html#readline_clear_history)
        — 清除历史
    -   [readline\_completion\_function](/ref/readline.html#readline_completion_function)
        — 注册一个完成函数
    -   [readline\_info](/ref/readline.html#readline_info) —
        获取/设置readline内部的各个变量
    -   [readline\_list\_history](/ref/readline.html#readline_list_history)
        — 获取命令历史列表
    -   [readline\_on\_new\_line](/ref/readline.html#readline_on_new_line)
        — 通知readline将光标移动到新行
    -   [readline\_read\_history](/ref/readline.html#readline_read_history)
        — 读取命令历史
    -   [readline\_redisplay](/ref/readline.html#readline_redisplay) —
        重绘显示区
    -   [readline\_write\_history](/ref/readline.html#readline_write_history)
        — 写入历史记录
    -   [readline](/ref/readline.html#readline) — 读取一行
