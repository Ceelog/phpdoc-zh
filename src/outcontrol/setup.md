安装／配置
==========

**目录**

-   [需求](/outcontrol/setup.html#需求)
-   [安装](/outcontrol/setup.html#安装)
-   [运行时配置](/outcontrol/setup.html#运行时配置)
-   [资源类型](/outcontrol/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

使用这些函数不需要安装，它们是 PHP 核心的一部分。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字              | 默认 | 可修改范围       | 更新日志                                   |
|-------------------|------|------------------|--------------------------------------------|
| output\_buffering | "0"  | PHP\_INI\_PERDIR |                                            |
| output\_handler   | NULL | PHP\_INI\_PERDIR | 自 PHP 4.0.4 起可用                        |
| implicit\_flush   | "0"  | PHP\_INI\_ALL    | 在 PHP \<= 4.2.3 版本中是 PHP\_INI\_PERDIR |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`output_buffering` <span class="type">boolean</span>/<span class="type">integer</span>  
该选项设置为 On
时，将在所有的脚本中使用输出控制。如果要限制输出缓冲区的最大值，可将该选项设定为指定的最大字节数（例如
output\_buffering=4096）。从PHP 4.3.5 版开始，该选项在 PHP-CLI 下总是为
Off。

`output_handler` <span class="type">string</span>  
该选项可将脚本所有的输出，重定向到一个函数。例如，将 output\_handler
设置为 <span class="function">mb\_output\_handler</span>
时，字符的编码将被修改为指定的编码。设置的任何处理函数，将自动的处理输出缓冲。

> **Note**:
>
> 不能同时使用 <span class="function">mb\_output\_handler</span> 和
> <span class="function">ob\_iconv\_handler</span>，也不能同时使用 <span
> class="function">ob\_gzhandler</span> 和
> <a href="/zlib/setup.html#" class="link">zlib.output_compression</a>。

> **Note**:
>
> 只有内置函数可以使用此指令。对于用户定义的函数，使用 <span
> class="function">ob\_start</span>。

`implicit_flush` <span class="type">boolean</span>  
默认为 **`FALSE`**。如将该选项改为 **`TRUE`**，PHP
将使输出层，在每段信息块输出后，自动刷新。这等同于在每次使用 <span
class="function">print</span>、<span class="function">echo</span>
等函数或每个 *HTML* 块之后，调用 PHP 中的 <span
class="function">flush</span> 函数。

不在web环境中使用 PHP
时，打开这个选项对程序执行的性能有严重的影响，通常只推荐在调试时使用。在
*CLI SAPI* 的执行模式下，该标记默认为 **`TRUE`**。

参见 <span class="function">ob\_implicit\_flush</span>。

资源类型
--------

此扩展没有定义资源类型。
