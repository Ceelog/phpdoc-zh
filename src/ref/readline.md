readline\_add\_history
======================

添加一行命令行历史记录

### 说明

<span class="type">bool</span> <span
class="methodname">readline\_add\_history</span> ( <span
class="methodparam"><span class="type">string</span> `$line`</span> )

这个函数添加一行到命令行历史记录 This function adds a line to the
command line history.

### 参数

`line`  
这一行将被添加到历史.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

readline\_callback\_handler\_install
====================================

初始化一个 readline 回调接口，然后终端输出提示信息并立即返回

### 说明

<span class="type">bool</span> <span
class="methodname">readline\_callback\_handler\_install</span> ( <span
class="methodparam"><span class="type">string</span> `$prompt`</span> ,
<span class="methodparam"><span class="type">callable</span>
`$callback`</span> )

设置一个 readline 回调接口然后输出 `prompt` 并立即返回.
第二次调用这个函数不需要移除上一个回调接口，这个函数将自动覆盖旧的接口.

当配合 <span class="function">stream\_select</span>
时回调的特性非常有用，它允许在 IO 与用户输入 间交叉进行，不像<span
class="function">readline</span>.

### 参数

`prompt`  
提示信息.

`callback`  
`callback` 函数需要一个参数; 用户输入将被返回.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 Readline Callback Interface Example**

``` php
<?php
function rl_callback($ret)
{
    global $c, $prompting;

    echo "You entered: $ret\n";
    $c++;

    if ($c > 10) {
        $prompting = false;
        readline_callback_handler_remove();
    } else {
        readline_callback_handler_install("[$c] Enter something: ", 'rl_callback');
    }
}

$c = 1;
$prompting = true;

readline_callback_handler_install("[$c] Enter something: ", 'rl_callback');

while ($prompting) {
    $w = NULL;
    $e = NULL;
    $n = stream_select($r = array(STDIN), $w, $e, null);
    if ($n && in_array(STDIN, $r)) {
        // read a character, will call the callback when a newline is entered
        readline_callback_read_char();
    }
}

echo "Prompting disabled. All done.\n";
?>
```

### 参见

-   <span class="function">readline\_callback\_handler\_remove</span>
-   <span class="function">readline\_callback\_read\_char</span>
-   <span class="function">stream\_select</span>

readline\_callback\_handler\_remove
===================================

移除上一个安装的回调函数句柄并且恢复终端设置

### 说明

<span class="type">bool</span> <span
class="methodname">readline\_callback\_handler\_remove</span> ( <span
class="methodparam">void</span> )

移除上一个安装的回调函数句柄并且恢复终端设置.

### 返回值

如果上一个被安装的回调函数句柄被移出返回 **`TRUE`** 否则 **`FALSE`**
如果没有找到的话.

### 范例

See <span class="function">readline\_callback\_handler\_install</span>
for an example of how to use the readline callback interface.

### 参见

-   <span class="function">readline\_callback\_handler\_install</span>
-   <span class="function">readline\_callback\_read\_char</span>

readline\_callback\_read\_char
==============================

当一个行被接收时读取一个字符并且通知 readline 调用回调函数

### 说明

<span class="type">void</span> <span
class="methodname">readline\_callback\_read\_char</span> ( <span
class="methodparam">void</span> )

读取用户输入中的一个字符.当一行被接收时，这个函数将通知 readline
调用使用 <span
class="function">readline\_callback\_handler\_install</span>
安装的回调函数接口，并且 这一个行已经准备输入.

### 返回值

没有返回值。

### 范例

See <span class="function">readline\_callback\_handler\_install</span>
for an example of how to use the readline callback interface.

### 参见

-   <span class="function">readline\_callback\_handler\_install</span>
-   <span class="function">readline\_callback\_handler\_remove</span>

readline\_clear\_history
========================

清除历史

### 说明

<span class="type">bool</span> <span
class="methodname">readline\_clear\_history</span> ( <span
class="methodparam">void</span> )

这个函数清除整个的命令行历史.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

readline\_completion\_function
==============================

注册一个完成函数

### 说明

<span class="type">bool</span> <span
class="methodname">readline\_completion\_function</span> ( <span
class="methodparam"><span class="type">callable</span>
`$function`</span> )

这个函数注册一个完成函数.这就像你在使用 Bash 时按 tab
键时你想要的功能一样

### 参数

`function`  
你必须提供一个已经存在的函数的名字并且可以接受命令行中的部分输入
然后返回一些可能匹配的数组.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

readline\_info
==============

获取/设置readline内部的各个变量

### 说明

<span class="type">mixed</span> <span
class="methodname">readline\_info</span> (\[ <span
class="methodparam"><span class="type">string</span> `$varname`</span>
\[, <span class="methodparam"><span class="type">string</span>
`$newvalue`</span> \]\] )

获取/设置readline内部的各个变量.

### 参数

`varname`  
变量名.

`newvalue`  
如果提供，将被设置成这个值.

### 返回值

如果调用时没有参数，这个函数将返回一个包括了所有已采用的readline设置的数组.
数组元素将索引是以下这些值：done, end, erase\_empty\_line,
library\_version, line\_buffer, mark, pending\_input, point, prompt,
readline\_name, and terminal\_name.

如果调用是提供了一个或两个参数，原来的值将被返回.

readline\_list\_history
=======================

获取命令历史列表

### 说明

<span class="type">array</span> <span
class="methodname">readline\_list\_history</span> ( <span
class="methodparam">void</span> )

获取整个命令行历史.

### 返回值

返回整个命令行历史的数组.元素的整数索引从零开始

readline\_on\_new\_line
=======================

通知readline将光标移动到新行

### 说明

<span class="type">void</span> <span
class="methodname">readline\_on\_new\_line</span> ( <span
class="methodparam">void</span> )

告诉readline将光标移动到新行.

### 返回值

没有返回值。

readline\_read\_history
=======================

读取命令历史

### 说明

<span class="type">bool</span> <span
class="methodname">readline\_read\_history</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\] )

这个函数从一个文件读取命令历史

### 参数

`filename`  
保存了命令历史的文件的路径.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

readline\_redisplay
===================

重绘显示区

### 说明

<span class="type">void</span> <span
class="methodname">readline\_redisplay</span> ( <span
class="methodparam">void</span> )

readline 重绘用于重绘显示区

### 返回值

没有返回值。

readline\_write\_history
========================

写入历史记录

### 说明

<span class="type">bool</span> <span
class="methodname">readline\_write\_history</span> (\[ <span
class="methodparam"><span class="type">string</span> `$filename`</span>
\] )

这个函数将命令历史写入到一个文件.

### 参数

`filename`  
保存文件的路径.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

readline
========

读取一行

### 说明

<span class="type">string</span> <span
class="methodname">readline</span> (\[ <span class="methodparam"><span
class="type">string</span> `$prompt`</span> \] )

从用户端读取一行.你必须自己使用 <span
class="function">readline\_add\_history</span> 将这一行添加到历史记录中

### 参数

`prompt`  
你可以指定一个字符串来作为用户的提示信息

### 返回值

从用户端返回一个行字符串.返回的该行的行尾换行符会被删除

### 范例

**示例 \#1 <span class="function">readline</span> Example**

``` php
<?php
//get 3 commands from user
for ($i=0; $i < 3; $i++) {
        $line = readline("Command: ");
        readline_add_history($line);
}

//dump history
print_r(readline_list_history());

//dump variables
print_r(readline_info());
?>
```

**目录**

-   [readline\_add\_history](/ref/readline.html#readline_add_history) —
    添加一行命令行历史记录
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
-   [readline\_on\_new\_line](/ref/readline.html#readline_on_new_line) —
    通知readline将光标移动到新行
-   [readline\_read\_history](/ref/readline.html#readline_read_history)
    — 读取命令历史
-   [readline\_redisplay](/ref/readline.html#readline_redisplay) —
    重绘显示区
-   [readline\_write\_history](/ref/readline.html#readline_write_history)
    — 写入历史记录
-   [readline](/ref/readline.html#readline) — 读取一行
