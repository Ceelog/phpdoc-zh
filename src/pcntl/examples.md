范例
====

**目录**

-   [](/pcntl/examples.html#)

这个示例用于产生一个守护进程并可以通过信号处理进行关闭。

**示例 \#1 进程控制示例**

``` php
<?php
//定义ticks
declare(ticks=1);

//产生子进程分支
$pid = pcntl_fork();
if ($pid == -1) {
     die("could not fork"); //pcntl_fork返回-1标明创建子进程失败
} else if ($pid) {
     exit(); //父进程中pcntl_fork返回创建的子进程进程号
} else {
     // 子进程pcntl_fork返回的时0
}

// 从当前终端分离
if (posix_setsid() == -1) {
    die("could not detach from terminal");
}

// 安装信号处理器
pcntl_signal(SIGTERM, "sig_handler");
pcntl_signal(SIGHUP, "sig_handler");

// 执行无限循环任务
while (1) {

    // do something interesting here

}

function sig_handler($signo) 
{

     switch ($signo) {
         case SIGTERM:
             // 处理中断信号
             exit;
             break;
         case SIGHUP:
             // 处理重启信号
             break;
         default:
             // 处理所有其他信号
     }

}

?>
```
