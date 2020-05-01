注释
----

**Warning**

以加锁方式打开的文件（特别是在打开会话时），
必须在执行后台程序之前关闭。

参见
----

这些函数和
<a href="/language/operators/execution.html" class="link">执行运算符</a>
是紧密关联的。 因此，当运行在
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">安全模式</a>
是，你必须考虑
<a href="/ini/sect/safe-mode.html#ini.safe-mode-exec-dir" class="link">safe_mode_exec_dir</a>
指示。

escapeshellarg
==============

把字符串转码为可以在 shell 命令里使用的参数

### 说明

<span class="type">string</span> <span
class="methodname">escapeshellarg</span> ( <span
class="methodparam"><span class="type">string</span> `$arg`</span> )

<span class="function">escapeshellarg</span>
将给字符串增加一个单引号并且能引用或者转码任何已经存在的单引号，这样以确保能够直接将一个字符串传入
shell
函数，并且还是确保安全的。对于用户输入的部分参数就应该使用这个函数。shell
函数包含 <span class="function">exec</span>, <span
class="function">system</span>
<a href="/language/operators/execution.html" class="link">执行运算符</a>
。

### 参数

`arg`  
需要被转码的参数。

### 返回值

转换之后字符串。

### 范例

**示例 \#1 <span class="function">escapeshellarg</span> 的例子**

``` php
<?php
system('ls '.escapeshellarg($dir));
?>
```

### 参见

-   <span class="function">escapeshellcmd</span>
-   <span class="function">exec</span>
-   <span class="function">popen</span>
-   <span class="function">system</span>
-   <a href="/language/operators/execution.html" class="link">执行运算符</a>

escapeshellcmd
==============

shell 元字符转义

### 说明

<span class="type">string</span> <span
class="methodname">escapeshellcmd</span> ( <span
class="methodparam"><span class="type">string</span> `$command`</span> )

<span class="function">escapeshellcmd</span> 对字符串中可能会欺骗 shell
命令执行任意命令的字符进行转义。 此函数保证用户输入的数据在传送到 <span
class="function">exec</span> 或 <span class="function">system</span>
函数，或者
<a href="/language/operators/execution.html" class="link">执行操作符</a>
之前进行转义。

反斜线（\\）会在以下字符之前插入： *&\#;\`\|\*?\~\<\>^()\[\]{}$\\*,
*\\x0A* 和 *\\xFF*。 *'* 和 *"* 仅在不配对儿的时候被转义。 在 Windows
平台上，所有这些字符以及 *%* 和 *!* 字符都会被空格代替。

### 参数

`command`  
要转义的命令。

### 返回值

转义后的字符串。

### 范例

**示例 \#1 <span class="function">escapeshellcmd</span> example**

``` php
<?php
// 我们故意允许任意数量的参数
$command = './configure '.$_POST['configure_options'];

$escaped_command = escapeshellcmd($command);
 
system($escaped_command);
?>
```

**Warning**

<span class="function">escapeshellcmd</span>
应被用在完整的命令字符串上。
即使如此，攻击者还是可以传入任意数量的参数。 请使用 <span
class="function">escapeshellarg</span> 函数 对单个参数进行转义。

### 更新日志

| 版本                   | 说明                   |
|------------------------|------------------------|
| 5.4.43, 5.5.27, 5.6.11 | 感叹号会被空格所替换。 |

### 参见

-   <span class="function">escapeshellarg</span>
-   <span class="function">exec</span>
-   <span class="function">popen</span>
-   <span class="function">system</span>
-   <a href="/language/operators/execution.html" class="link">执行运算符</a>

exec
====

执行一个外部程序

### 说明

<span class="type">string</span> <span class="methodname">exec</span> (
<span class="methodparam"><span class="type">string</span>
`$command`</span> \[, <span class="methodparam"><span
class="type">array</span> `&$output`</span> \[, <span
class="methodparam"><span class="type">int</span> `&$return_var`</span>
\]\] )

<span class="function">exec</span> 执行 `command` 参数所指定的命令。

### 参数

`command`  
要执行的命令。

`output`  
如果提供了 `output` 参数， 那么会用命令执行的输出填充此数组，
每行输出填充数组中的一个元素。 数组中的数据不包含行尾的空白字符，例如
*\\n* 字符。 请注意，如果数组中已经包含了部分元素，<span
class="function">exec</span>
函数会在数组末尾追加内容。如果你不想在数组末尾进行追加， 请在传入 <span
class="function">exec</span> 函数之前 对数组使用 <span
class="function">unset</span> 函数进行重置。

`return_var`  
如果同时提供 `output` 和 `return_var` 参数，
命令执行后的返回状态会被写入到此变量。

### 返回值

命令执行结果的最后一行内容。 如果你需要获取未经处理的全部输出数据，
请使用 <span class="function">passthru</span> 函数。

如果想要获取命令的输出内容， 请确保使用 `output` 参数。

### 范例

**示例 \#1 <span class="function">exec</span> 例程**

``` php
<?php
// 输出运行中的 php/httpd 进程的创建者用户名
// （在可以执行 "whoami" 命令的系统上）
echo exec('whoami');
?>
```

### 注释

**Warning**

当用户提供的数据传入此函数，使用 <span
class="function">escapeshellarg</span> 或 <span
class="function">escapeshellcmd</span>
来确保用户欺骗系统从而执行任意命令。

> **Note**:
>
> 如何程序使用此函数启动，为了能保持在后台运行，此程序必须将输出重定向到文件或其它输出流。否则会导致
> PHP 挂起，直至程序执行结束。

> **Note**:
>
> On Windows <span class="function">exec</span> will first start cmd.exe
> to launch the command. If you want to start an external program
> without starting cmd.exe use <span class="function">proc\_open</span>
> with the `bypass_shell` option set.

> **Note**: <span
> class="simpara"><a href="/features/safe-mode.html" class="link">安全模式</a>
> 启用时，可仅可用
> <a href="/ini/sect/safe-mode.html#ini.safe-mode-exec-dir" class="link">safe_mode_exec_dir</a>
> 执行文件。实际上，现在不允许在到可执行的路径中存在 *..* 组件。</span>

**Warning**

<a href="/features/safe-mode.html" class="link">安全模式</a>
启用时，命令字符串会被 <span class="function">escapeshellcmd</span>
转换。因此，*echo y \| echo x* 会变成 *echo y \\\| echo x*。

### 参见

-   <span class="function">system</span>
-   <span class="function">passthru</span>
-   <span class="function">escapeshellcmd</span>
-   <span class="function">pcntl\_exec</span>
-   <a href="/language/operators/execution.html" class="link">执行运算符</a>

passthru
========

执行外部程序并且显示原始输出

### 说明

<span class="type">void</span> <span class="methodname">passthru</span>
( <span class="methodparam"><span class="type">string</span>
`$command`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$return_var`</span> \] )

同 <span class="function">exec</span> 函数类似， <span
class="function">passthru</span> 函数
也是用来执行外部命令（`command`）的。 当所执行的 Unix
命令输出二进制数据， 并且需要直接传送到浏览器的时候， 需要用此函数来替代
<span class="function">exec</span> 或 <span
class="function">system</span> 函数。 常用来执行诸如 pbmplus
之类的可以直接输出图像流的命令。 通过设置 Content-type 为 *image/gif*，
然后调用 pbmplus 程序输出 gif 文件， 就可以从 PHP
脚本中直接输出图像到浏览器。

### 参数

`command`  
要执行的命令。

`return_var`  
如果提供 `return_var` 参数， Unix 命令的返回状态会被记录到此参数。

### 返回值

没有返回值。

### 注释

**Warning**

当用户提供的数据传入此函数，使用 <span
class="function">escapeshellarg</span> 或 <span
class="function">escapeshellcmd</span>
来确保用户欺骗系统从而执行任意命令。

> **Note**:
>
> 如何程序使用此函数启动，为了能保持在后台运行，此程序必须将输出重定向到文件或其它输出流。否则会导致
> PHP 挂起，直至程序执行结束。

> **Note**: <span
> class="simpara"><a href="/features/safe-mode.html" class="link">安全模式</a>
> 启用时，可仅可用
> <a href="/ini/sect/safe-mode.html#ini.safe-mode-exec-dir" class="link">safe_mode_exec_dir</a>
> 执行文件。实际上，现在不允许在到可执行的路径中存在 *..* 组件。</span>

**Warning**

<a href="/features/safe-mode.html" class="link">安全模式</a>
启用时，命令字符串会被 <span class="function">escapeshellcmd</span>
转换。因此，*echo y \| echo x* 会变成 *echo y \\\| echo x*。

### 参见

-   <span class="function">exec</span>
-   <span class="function">system</span>
-   <span class="function">popen</span>
-   <span class="function">escapeshellcmd</span>
-   <a href="/language/operators/execution.html" class="link">执行运算符</a>

proc\_close
===========

关闭由 <span class="function">proc\_open</span>
打开的进程并且返回进程退出码

### 说明

<span class="type">int</span> <span
class="methodname">proc\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$process`</span> )

<span class="function">proc\_close</span> 同 <span
class="function">pclose</span> 函数类似， 只是 <span
class="function">proc\_close</span> 只能用来关闭由 <span
class="function">proc\_open</span> 函数打开的进程。 <span
class="function">proc\_close</span> 函数会等待进程终止，
并且返回进程的返回值。 如果有连接到进程的已经打开的管道，
那么需要在调用此函数之前调用 <span class="function">fclose</span>
函数来关闭管道， 否则会引发死锁 -
在管道处于打开状态时，子进程将不能退出。

### 参数

`process`  
要关闭的由 <span class="function">proc\_open</span> 打开的 <span
class="type">resource</span> 。

### 返回值

返回进程的终止状态码。 如果发生错误，将返回 *-1*。

> **Note**:
>
> If PHP has been compiled with --enable-sigchild, the return value of
> this function is undefined.

proc\_get\_status
=================

获取由 <span class="function">proc\_open</span> 函数打开的进程的信息

### 说明

<span class="type">array</span> <span
class="methodname">proc\_get\_status</span> ( <span
class="methodparam"><span class="type">resource</span> `$process`</span>
)

<span class="function">proc\_get\_status</span> 函数可以获取由 <span
class="function">proc\_open</span> 函数打开的进程的信息。

### 参数

`process`  
要检查的由 <span class="function">proc\_open</span> 打开的进程 <span
class="type">resource</span>。

### 返回值

如果调用成功，则返回一个包含了进程信息的 <span
class="type">array</span>，如果发生错误，返回 **`FALSE`**。
返回的数组包含下列元素：

| 元素     | 类型                             | 描述                                                                                                                    |
|----------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| command  | <span class="type">string</span> | 传入 <span class="function">proc\_open</span> 函数的命令行字符串。                                                      |
| pid      | <span class="type">int</span>    | 进程 ID                                                                                                                 |
| running  | <span class="type">bool</span>   | **`TRUE`** 表示进程还在运行中， **`FALSE`** 表示进程已经终止                                                            |
| signaled | <span class="type">bool</span>   | **`TRUE`** 表示子进程被未捕获的信号所终止。 在 Windows 平台永远为 **`FALSE`**。                                         |
| stopped  | <span class="type">bool</span>   | **`TRUE`** 表示子进程被信号停止。 在 Windows 平台永远为 **`FALSE`**。                                                   |
| exitcode | <span class="type">int</span>    | 进程的退出码（仅在 *running* 为 **`FALSE`** 时有意义）。 仅在第一次调用此函数时会返回实际的值， 后续的调用将返回 *-1*。 |
| termsig  | <span class="type">int</span>    | 导致子进程终止执行的信号值 （仅在 *signaled* 为 **`TRUE`** 时有意义）。                                                 |
| stopsig  | <span class="type">int</span>    | 导致子进程停止执行的信号值 （仅在 *stopped* 为 **`TRUE`** 时有意义）。                                                  |

### 参见

-   <span class="function">proc\_open</span>

proc\_nice
==========

修改当前进程的优先级

### 说明

<span class="type">bool</span> <span
class="methodname">proc\_nice</span> ( <span class="methodparam"><span
class="type">int</span> `$increment`</span> )

<span class="function">proc\_nice</span> 修改当前进程的优先级， 修改量由
`increment` 参数指定。 `increment` 为正数会降低当前进程优先级，
反之，为负数会提高优先级。

<span class="function">proc\_nice</span> 和 <span
class="function">proc\_open</span> 函数以及和 <span
class="function">proc\_open</span> 相关的函数并无什么关系。

### 参数

`increment`  
新的优先级值，具体的设定取决于所运行的平台。

在 Unix 系统上，较小的值表示较高的优先级，例如：*-20*，
而正数值表示更低的优先级。

在 Windows 平台上，`increment` 参数 的含义如下：

| 优先级     | 可能的值                                 |
|------------|------------------------------------------|
| 高优先级   | `increment` *\< -9*                      |
| 较高优先级 | `increment` *\< -4*                      |
| 正常优先级 | `increment` *\< 5* & `increment` *\> -5* |
| 较低优先级 | `increment` *\> 5*                       |
| 低优先级   | `increment` *\> 9*                       |

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。。
如果发生错误，例如用户无权修改当前进程的优先级， 会生成 **`E_WARNING`**
级别的错误。

### 范例

**示例 \#1 使用 <span class="function">proc\_open</span>
函数将进程设置为高优先级**

``` php
<?php
// Highest priority
proc_nice(-20);
?>
```

### 更新日志

| 版本  | 说明                    |
|-------|-------------------------|
| 7.2.0 | 在 Windows 平台上可用。 |

### 注释

> **Note**: **可用性**  
>
> 仅在具有 'nice' 能力的系统上才可以使用 <span
> class="function">proc\_nice</span> 函数。 下列系统含有 'nice'：SVr4,
> SVID EXT, AT&T, X/OPEN, BSD 4.3。

> **Note**: **Windows 平台**  
>
> <span class="function">proc\_nice</span> 函数会改变 *当前*
> 进程优先级，即使 PHP 是使用线程安全模式编译的。

proc\_open
==========

执行一个命令，并且打开用来输入/输出的文件指针。

### 说明

<span class="type">resource</span> <span
class="methodname">proc\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$cmd`</span> , <span
class="methodparam"><span class="type">array</span>
`$descriptorspec`</span> , <span class="methodparam"><span
class="type">array</span> `&$pipes`</span> \[, <span
class="methodparam"><span class="type">string</span> `$cwd`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$env`<span
class="initializer"> = **`NULL`**</span></span> \[, <span
class="methodparam"><span class="type">array</span>
`$other_options`<span class="initializer"> = **`NULL`**</span></span>
\]\]\] )

类似 <span class="function">popen</span> 函数， 但是 <span
class="function">proc\_open</span> 提供了更加强大的控制程序执行的能力。

### 参数

`cmd`  
要执行的命令

`descriptorspec`  
一个索引数组。 数组的键表示描述符，数组元素值表示 PHP
如何将这些描述符传送至子进程。 0 表示标准输入（stdin），1
表示标准输出（stdout），2 表示标准错误（stderr）。

数组中的元素可以是：

-   包含了要传送至进程的管道的描述信息。 第一个元素为描述符类型，
    第二个元素是针对该描述符的选项。 有效的类型有：*pipe*
    （第二个元素可以是： *r* 向进程传送该管道的读取端，*w*
    向进程传送该管道的写入端）， 以及 *file*（第二个元素为文件名）。
-   表达一个真实文件描述符的流资源类型 （例如：已打开的文件，一个 socket
    端口，**`STDIN`**）。

文件描述符的值不限于 0，1 和 2，你可以使用任何有效的文件描述符
并将其传送至子进程。 这使得你的脚本可以和其他脚本交互操作。
例如，可以通过指定文件描述符将密码以更加安全的方式 传送至诸如 PGP，GPG
和 openssl 程序， 同时也可以很方便的获取这些程序的状态信息。

`pipes`  
将被置为索引数组， 其中的元素是被执行程序创建的管道对应到 PHP
这一端的文件指针。

`cwd`  
要执行命令的初始工作目录。 必须是 *绝对* 路径， 设置此参数为 **`NULL`**
表示使用默认值（当前 PHP 进程的工作目录）。

`env`  
要执行的命令所使用的环境变量。 设置此参数为 **`NULL`** 表示使用和当前
PHP 进程相同的环境变量。

`other_options`  
你还可以指定一些附加选项。 目前支持的选项包括：

-   *suppress\_errors* （仅用于 Windows 平台）： 设置为 **`TRUE`**
    表示抑制本函数产生的错误。
-   *bypass\_shell* （仅用于 Windows 平台）： 设置为 **`TRUE`** 表示绕过
    *cmd.exe* shell。

### 返回值

返回表示进程的资源类型， 当使用完毕之后，请调用 <span
class="function">proc\_close</span> 函数来关闭此资源。 如果失败，返回
**`FALSE`**。

### 更新日志

| 版本  | 说明                                               |
|-------|----------------------------------------------------|
| 5.2.1 | 为 `other_options` 参数增加 *bypass\_shell* 选项。 |

### 范例

**示例 \#1 <span class="function">proc\_open</span> 例程**

``` php
<?php
$descriptorspec = array(
   0 => array("pipe", "r"),  // 标准输入，子进程从此管道中读取数据
   1 => array("pipe", "w"),  // 标准输出，子进程向此管道中写入数据
   2 => array("file", "/tmp/error-output.txt", "a") // 标准错误，写入到一个文件
);

$cwd = '/tmp';
$env = array('some_option' => 'aeiou');

$process = proc_open('php', $descriptorspec, $pipes, $cwd, $env);

if (is_resource($process)) {
    // $pipes 现在看起来是这样的：
    // 0 => 可以向子进程标准输入写入的句柄
    // 1 => 可以从子进程标准输出读取的句柄
    // 错误输出将被追加到文件 /tmp/error-output.txt

    fwrite($pipes[0], '<?php print_r($_ENV); ?>');
    fclose($pipes[0]);

    echo stream_get_contents($pipes[1]);
    fclose($pipes[1]);
    

    // 切记：在调用 proc_close 之前关闭所有的管道以避免死锁。
    $return_value = proc_close($process);

    echo "command returned $return_value\n";
}
?>
```

以上例程的输出类似于：

    Array
    (
        [some_option] => aeiou
        [PWD] => /tmp
        [SHLVL] => 1
        [_] => /usr/local/bin/php
    )
    command returned 0

### 注释

> **Note**:
>
> Windows 兼容性：超过 2 的描述符也可以作为可继承的句柄传送到子进程。
> 但是，由于 Windows 的架构并不将文件描述符和底层句柄进行关联，
> 所以，子进程无法访问这样的句柄。
> 标准输入，标准输出和标注错误会按照预期工作。

> **Note**:
>
> 如果你只需要单向的进程管道， 使用 <span class="function">popen</span>
> 函数会更加简单。

### 参见

-   <span class="function">popen</span>
-   <span class="function">exec</span>
-   <span class="function">system</span>
-   <span class="function">passthru</span>
-   <span class="function">stream\_select</span>
-   The
    <a href="/language/operators/execution.html" class="link">执行操作符</a>

proc\_terminate
===============

杀除由 proc\_open 打开的进程

### 说明

<span class="type">bool</span> <span
class="methodname">proc\_terminate</span> ( <span
class="methodparam"><span class="type">resource</span> `$process`</span>
\[, <span class="methodparam"><span class="type">int</span>
`$signal`<span class="initializer"> = 15</span></span> \] )

向 `process` （由 <span class="function">proc\_open</span> 函数创建）
发送信号通知其终止。 <span class="function">proc\_terminate</span>
调用之后将会立即返回， 而不会等待进程终止。

可以使用 <span class="function">proc\_terminate</span> 终止进程
并且继续其他的任务。 可以使用 <span
class="function">proc\_get\_status</span> 函数来检查进程是否已经终止。

### 参数

`process`  
由 <span class="function">proc\_open</span> 打开的 <span
class="type">resource</span>。

`signal`  
可选参数，仅用于 POSIX 操作系统。 表示调用系统命令 *kill(2)*
来向进程发送的信号。 默认值为 *SIGTERM*。

### 返回值

返回进程的终止状态。

### 更新日志

| 版本  | 说明                                  |
|-------|---------------------------------------|
| 5.2.2 | 之前的版本被用来销毁进程 `resource`。 |

### 参见

-   <span class="function">proc\_open</span>
-   <span class="function">proc\_close</span>
-   <span class="function">proc\_get\_status</span>

shell\_exec
===========

通过 shell 环境执行命令，并且将完整的输出以字符串的方式返回。

### 说明

<span class="type">string</span> <span
class="methodname">shell\_exec</span> ( <span class="methodparam"><span
class="type">string</span> `$cmd`</span> )

本函数同
<a href="/language/operators/execution.html" class="link">执行操作符</a>。

### 参数

`cmd`  
要执行的命令。

### 返回值

命令执行的输出。 如果执行过程中发生错误或者进程不产生输出，则返回
**`NULL`**。

> **Note**:
>
> 当进程执行过程中发生错误，或者进程不产生输出的情况下，都会返回
> **`NULL`**， 所以，使用本函数无法通过返回值检测进程是否成功执行。
> 如果需要检查进程执行的退出码，请使用 <span
> class="function">exec</span> 函数。

### 范例

**示例 \#1 <span class="function">shell\_exec</span> 例程**

``` php
<?php
$output = shell_exec('ls -lart');
echo "<pre>$output</pre>";
?>
```

### 注释

> **Note**:
>
> 当 PHP 运行在
> <a href="/features/safe-mode.html" class="link">安全模式</a>
> 时，不能使用此函数。

### 参见

-   <span class="function">exec</span>
-   <span class="function">escapeshellcmd</span>

system
======

执行外部程序，并且显示输出

### 说明

<span class="type">string</span> <span class="methodname">system</span>
( <span class="methodparam"><span class="type">string</span>
`$command`</span> \[, <span class="methodparam"><span
class="type">int</span> `&$return_var`</span> \] )

同 C 版本的 <span class="function">system</span> 函数一样， 本函数执行
`command` 参数所指定的命令， 并且输出执行结果。

如果 PHP 运行在服务器模块中， <span class="function">system</span>
函数还会尝试在每行输出完毕之后， 自动刷新 web 服务器的输出缓存。

如果要获取一个命令未经任何处理的 原始输出， 请使用 <span
class="function">passthru</span> 函数。

### 参数

`command`  
要执行的命令。

`return_var`  
如果提供 `return_var` 参数，
则外部命令执行后的返回状态将会被设置到此变量中。

### 返回值

成功则返回命令输出的最后一行， 失败则返回 **`FALSE`**

### 范例

**示例 \#1 <span class="function">system</span> 例程**

``` php
<?php
echo '<pre>';

// 输出 shell 命令 "ls" 的返回结果
// 并且将输出的最后一样内容返回到 $last_line。
// 将命令的返回值保存到 $retval。
$last_line = system('ls', $retval);

// 打印更多信息
echo '
</pre>
<hr />Last line of the output: ' . $last_line . '
<hr />Return value: ' . $retval;
?>
```

### 注释

**Warning**

当用户提供的数据传入此函数，使用 <span
class="function">escapeshellarg</span> 或 <span
class="function">escapeshellcmd</span>
来确保用户欺骗系统从而执行任意命令。

> **Note**:
>
> 如何程序使用此函数启动，为了能保持在后台运行，此程序必须将输出重定向到文件或其它输出流。否则会导致
> PHP 挂起，直至程序执行结束。

> **Note**: <span
> class="simpara"><a href="/features/safe-mode.html" class="link">安全模式</a>
> 启用时，可仅可用
> <a href="/ini/sect/safe-mode.html#ini.safe-mode-exec-dir" class="link">safe_mode_exec_dir</a>
> 执行文件。实际上，现在不允许在到可执行的路径中存在 *..* 组件。</span>

**Warning**

<a href="/features/safe-mode.html" class="link">安全模式</a>
启用时，命令字符串会被 <span class="function">escapeshellcmd</span>
转换。因此，*echo y \| echo x* 会变成 *echo y \\\| echo x*。

### 参见

-   <span class="function">exec</span>
-   <span class="function">passthru</span>
-   <span class="function">popen</span>
-   <span class="function">escapeshellcmd</span>
-   <span class="function">pcntl\_exec</span>
-   <a href="/language/operators/execution.html" class="link">执行操作符</a>

**目录**

-   [escapeshellarg](/ref/exec.html#escapeshellarg) —
    把字符串转码为可以在 shell 命令里使用的参数
-   [escapeshellcmd](/ref/exec.html#escapeshellcmd) — shell 元字符转义
-   [exec](/ref/exec.html#exec) — 执行一个外部程序
-   [passthru](/ref/exec.html#passthru) — 执行外部程序并且显示原始输出
-   [proc\_close](/ref/exec.html#proc_close) — 关闭由 proc\_open
    打开的进程并且返回进程退出码
-   [proc\_get\_status](/ref/exec.html#proc_get_status) — 获取由
    proc\_open 函数打开的进程的信息
-   [proc\_nice](/ref/exec.html#proc_nice) — 修改当前进程的优先级
-   [proc\_open](/ref/exec.html#proc_open) —
    执行一个命令，并且打开用来输入/输出的文件指针。
-   [proc\_terminate](/ref/exec.html#proc_terminate) — 杀除由 proc\_open
    打开的进程
-   [shell\_exec](/ref/exec.html#shell_exec) — 通过 shell
    环境执行命令，并且将完整的输出以字符串的方式返回。
-   [system](/ref/exec.html#system) — 执行外部程序，并且显示输出
