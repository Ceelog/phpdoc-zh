FastCGI 进程管理器（FPM）
=========================

**目录**

-   [安装](/install/fpm/install.html)
-   [配置](/install/fpm/configuration.html)

FPM（FastCGI 进程管理器）用于替换 PHP FastCGI
的大部分附加功能，对于高负载网站是非常有用的。

它的功能包括：

-   支持平滑停止/启动的高级进程管理功能；

-   可以工作于不同的 uid/gid/chroot 环境下，并监听不同的端口和使用不同的
    php.ini 配置文件（可取代 safe\_mode 的设置）；

-   stdout 和 stderr 日志记录;

-   在发生意外情况的时候能够重新启动并缓存被破坏的 opcode;

-   文件上传优化支持;

-   "慢日志" - 记录脚本（不仅记录文件名，还记录 PHP backtrace
    信息，可以使用
    ptrace或者类似工具读取和分析远程进程的运行数据）运行所导致的异常缓慢;

-   <span class="function">fastcgi\_finish\_request</span> -
    特殊功能：用于在请求完成和刷新数据后，继续在后台执行耗时的工作（录入视频转换、统计处理等）；

-   动态／静态子进程产生；

-   基本 SAPI 运行状态信息（类似Apache的 mod\_status）；

-   基于 php.ini 的配置文件。
