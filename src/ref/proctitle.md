setproctitle
============

Set the process title

### 说明

<span class="type">void</span> <span
class="methodname">setproctitle</span> ( <span class="methodparam"><span
class="type">string</span> `$title`</span> )

Sets the process title of the current process.

### 参数

`title`  
The title to use as the process title.

### 返回值

没有返回值。

### 范例

**示例 \#1 <span class="function">setproctitle</span> example**

Running the example below will change the process title (visible with
*ps a* for example).

``` php
<?php
setproctitle("myscript");
?>
```

以上例程的输出类似于：

    $ ps a
      PID TTY      STAT   TIME COMMAND
     1168 pts/3    S      0:00 myscript                                                                                                                         

### 参见

-   <span class="function">cli\_set\_process\_title</span>
-   <span class="function">pcntl\_fork</span>
-   <span class="function">setthreadtitle</span>

setthreadtitle
==============

Set the thread title

### 说明

<span class="type">bool</span> <span
class="methodname">setthreadtitle</span> ( <span
class="methodparam"><span class="type">string</span> `$title`</span> )

Sets the thread title.

### 参数

`title`  
The title to use as the thread title.

### 返回值

成功时返回 **`true`**， 或者在失败时返回 **`false`**。

### 范例

**示例 \#1 <span class="function">setthreadtitle</span> example**

Running the example below will change the thread title (visible with *ps
c* for example).

``` php
<?php
setthreadtitle("myscript");
?>
```

以上例程的输出类似于：

    $ ps c
      PID TTY      STAT   TIME COMMAND
     1178 pts/3    S      0:00 myscript

### 参见

-   <span class="function">pcntl\_fork</span>
-   <span class="function">setproctitle</span>

**目录**

-   [setproctitle](/ref/proctitle.html#setproctitle) — Set the process
    title
-   [setthreadtitle](/ref/proctitle.html#setthreadtitle) — Set the
    thread title
