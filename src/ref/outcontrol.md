See also <span class="function">header</span> and <span
class="function">setcookie</span>.

flush
=====

刷新输出缓冲

### 说明

<span class="type">void</span> <span class="methodname">flush</span> (
<span class="methodparam">void</span> )

刷新PHP程序的缓冲，而不论PHP执行在何种情况下（CGI
，web服务器等等）。该函数将当前为止程序的所有输出发送到用户的浏览器。

<span class="function">flush</span>
函数不会对服务器或客户端浏览器的缓存模式产生影响。因此，必须同时使用
<span class="function">ob\_flush</span> 和<span
class="function">flush</span> 函数来刷新输出缓冲。

个别web服务器程序，特别是Win32下的web服务器程序，在发送结果到浏览器之前，仍然会缓存脚本的输出，直到程序结束为止。

有些Apache的模块，比如mod\_gzip，可能自己进行输出缓存，这将导致<span
class="function">flush</span>函数产生的结果不会立即被发送到客户端浏览器。

甚至浏览器也会在显示之前，缓存接收到的内容。例如 Netscape
浏览器会在接受到换行或 html 标记的开头之前缓存内容，并且在接受到
\</table\> 标记之前，不会显示出整个表格。

一些版本的 Microsoft Internet Explorer
只有当接受到的256个字节以后才开始显示该页面，所以必须发送一些额外的空格来让这些浏览器显示页面内容。

ob\_clean
=========

清空（擦掉）输出缓冲区

### 说明

<span class="type">void</span> <span class="methodname">ob\_clean</span>
( <span class="methodparam">void</span> )

此函数用来丢弃输出缓冲区中的内容。

此函数不会像 <span class="function">ob\_end\_clean</span>
函数那样销毁输出缓冲区。

输出缓冲必须已被 <span class="function">ob\_start</span> 以
<a href="/outcontrol/constants.html#" class="link">PHP_OUTPUT_HANDLER_CLEANABLE</a>
标记启动。否则 <span class="function">ob\_clean</span> 不会有效果。

### 返回值

没有返回值。

### 参见

-   <span class="function">ob\_flush</span>
-   <span class="function">ob\_end\_flush</span>
-   <span class="function">ob\_end\_clean</span>

ob\_end\_clean
==============

清空（擦除）缓冲区并关闭输出缓冲

### 说明

<span class="type">bool</span> <span
class="methodname">ob\_end\_clean</span> ( <span
class="methodparam">void</span> )

此函数丢弃最顶层输出缓冲区的内容并关闭这个缓冲区。如果想要进一步处理缓冲区的内容，必须在<span
class="function">ob\_end\_clean</span>之前调用<span
class="function">ob\_get\_contents</span>，因为当调用<span
class="function">ob\_end\_clean</span>时缓冲区内容将被丢弃。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。
错误的原因首先是，在调用时没有一个起作用的缓冲区，或者是因为某些原因缓冲区不能被删除（可能对特殊缓冲区而言）。

### 错误／异常

如果函数失败了，将引发一个**`E_NOTICE`**异常。

### 更新日志

| 版本  | 说明               |
|-------|--------------------|
| 4.2.0 | 添加了布尔返回值。 |

### 范例

下面的例子给出了一种去除所有输出缓冲区的方法：

**示例 \#1 <span class="function">ob\_end\_clean</span> example**

``` php
<?php
ob_start();
echo 'Text that won\'t get displayed.';
ob_end_clean();
?>
```

### 参见

-   <span class="function">ob\_start</span>
-   <span class="function">ob\_get\_contents</span>
-   <span class="function">ob\_flush</span>

ob\_end\_flush
==============

冲刷出（送出）输出缓冲区内容并关闭缓冲

### 说明

<span class="type">bool</span> <span
class="methodname">ob\_end\_flush</span> ( <span
class="methodparam">void</span> )

这个函数将送出最顶层缓冲区的内容（如果里边有内容的话），并关闭缓冲区。如果想进一步处理缓冲区中的内容，必须在<span
class="function">ob\_end\_flush</span>之前调用 <span
class="function">ob\_get\_contents</span>，因为在调用<span
class="function">ob\_end\_flush</span>后缓冲区内容被丢弃。

> **Note**: <span class="simpara"> 这个函数与<span
> class="function">ob\_get\_flush</span>相似，不同的是<span
> class="function">ob\_get\_flush</span>会把缓冲区中的内容作为字符串返回。
> </span>

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。
错误的原因首先是，在调用时没有一个起作用的缓冲区，或者是因为某些原因缓冲区不能被删除（可能对特殊缓冲区而言）。

### 错误／异常

如果函数失败了，将引发一个**`E_NOTICE`**异常。

### 更新日志

| 版本  | 说明               |
|-------|--------------------|
| 4.2.0 | 添加了布尔返回值。 |

### 范例

**示例 \#1 <span class="function">ob\_end\_flush</span> example**

下面的例子给出了一种送出缓冲区内容并关闭所有输出缓冲区的容易的方法：

``` php
<?php
  while (@ob_end_flush());
?>
```

### 参见

-   <span class="function">ob\_start</span>
-   <span class="function">ob\_get\_contents</span>
-   <span class="function">ob\_get\_flush</span>
-   <span class="function">ob\_flush</span>
-   <span class="function">ob\_end\_clean</span>

ob\_flush
=========

冲刷出（送出）输出缓冲区中的内容

### 说明

<span class="type">void</span> <span class="methodname">ob\_flush</span>
( <span class="methodparam">void</span> )

这个函数将送出缓冲区的内容（如果里边有内容的话）。如果想进一步处理缓冲区中的内容，必须在<span
class="function">ob\_flush</span>之前调用<span
class="function">ob\_get\_contents</span> ，因为在调用<span
class="function">ob\_flush</span>之后缓冲区内容将被丢弃。

此函数不会销毁输出缓冲区，而像<span
class="function">ob\_end\_flush</span> 函数会销毁缓冲区。

### 返回值

没有返回值。

### 参见

-   <span class="function">ob\_get\_contents</span>
-   <span class="function">ob\_clean</span>
-   <span class="function">ob\_end\_flush</span>
-   <span class="function">ob\_end\_clean</span>

ob\_get\_clean
==============

得到当前缓冲区的内容并删除当前输出缓。

### 说明

<span class="type">string</span> <span
class="methodname">ob\_get\_clean</span> ( <span
class="methodparam">void</span> )

得到当前缓冲区的内容并删除当前输出缓冲区。

<span class="function">ob\_get\_clean</span> 实质上是一起执行了 <span
class="function">ob\_get\_contents</span> 和 <span
class="function">ob\_end\_clean</span>。

### 返回值

返回输出缓冲区的内容，并结束输出缓冲区。如果输出缓冲区不是活跃的，即返回
**`FALSE`** 。

### 范例

**示例 \#1 A simple <span class="function">ob\_get\_clean</span>
example**

``` php
<?php

ob_start();

echo "Hello World";

$out = ob_get_clean();
$out = strtolower($out);

var_dump($out);
?>
```

以上例程会输出：


    string(11) "hello world"

### 参见

-   <span class="function">ob\_get\_contents</span>
-   <span class="function">ob\_start</span>

ob\_get\_contents
=================

返回输出缓冲区的内容

### 说明

<span class="type">string</span> <span
class="methodname">ob\_get\_contents</span> ( <span
class="methodparam">void</span> )

只是得到输出缓冲区的内容，但不清除它。

### 返回值

此函数返回输出缓冲区的内容，或者如果输出缓冲区无效将返回**`FALSE`** 。

### 范例

**示例 \#1 A simple <span class="function">ob\_get\_contents</span>
example**

``` php
<?php

ob_start();

echo "Hello ";

$out1 = ob_get_contents();

echo "World";

$out2 = ob_get_contents();

ob_end_clean();

var_dump($out1, $out2);
?>
```

以上例程会输出：

    string(6) "Hello "
    string(11) "Hello World"

### 参见

-   <span class="function">ob\_start</span>
-   <span class="function">ob\_get\_length</span>

ob\_get\_flush
==============

刷出（送出）缓冲区内容，以字符串形式返回内容，并关闭输出缓冲区。

### 说明

<span class="type">string</span> <span
class="methodname">ob\_get\_flush</span> ( <span
class="methodparam">void</span> )

<span class="function">ob\_get\_flush</span>
刷出（送出）缓冲区内容，以字符串形式返回内容，并关闭输出缓冲区。

> **Note**: <span class="simpara"> 这个函数与<span
> class="function">ob\_end\_flush</span>相似，不同的是本函数还会以字符串形式返回缓冲区内容。
> </span>

### 返回值

返回输出缓冲区的内容；或者是，如果没有起作用的输出缓冲区，返回**`FALSE`**
。

### 范例

**示例 \#1 <span class="function">ob\_get\_flush</span> example**

``` php
<?php
//using output_buffering=On
print_r(ob_list_handlers());

//save buffer in a file
$buffer = ob_get_flush();
file_put_contents('buffer.txt', $buffer);

print_r(ob_list_handlers());
?>
```

以上例程会输出：

    Array
    (
        [0] => default output handler
    )
    Array
    (
    )

### 参见

-   <span class="function">ob\_end\_clean</span>
-   <span class="function">ob\_end\_flush</span>
-   <span class="function">ob\_list\_handlers</span>

ob\_get\_length
===============

返回输出缓冲区内容的长度

### 说明

<span class="type">int</span> <span
class="methodname">ob\_get\_length</span> ( <span
class="methodparam">void</span> )

此函数将返回输出缓中冲区内容的长度。

### 返回值

返回输出缓冲区内容的长度；或者返回**`FALSE`**——如果没有起作用的缓冲区。

### 范例

**示例 \#1 A simple <span class="function">ob\_get\_length</span>
example**

``` php
<?php

ob_start();

echo "Hello ";

$len1 = ob_get_length();

echo "World";

$len2 = ob_get_length();

ob_end_clean();

echo $len1 . ", ." . $len2;
?>
```

以上例程会输出：

    6, 11

### 参见

-   <span class="function">ob\_start</span>
-   <span class="function">ob\_get\_contents</span>

ob\_get\_level
==============

返回输出缓冲机制的嵌套级别

### 说明

<span class="type">int</span> <span
class="methodname">ob\_get\_level</span> ( <span
class="methodparam">void</span> )

返回输出缓冲机制的嵌套级别。

### 返回值

返回嵌套的输出缓冲处理程序的级别；或者是，如果输出缓冲区不起作用，返回零。

### 参见

-   <span class="function">ob\_start</span>
-   <span class="function">ob\_get\_contents</span>

ob\_get\_status
===============

得到所有输出缓冲区的状态

### 说明

<span class="type">array</span> <span
class="methodname">ob\_get\_status</span> (\[ <span
class="methodparam"><span class="type">bool</span> `$full_status` <span
class="initializer"> = FALSE</span></span> \] )

<span
class="function">ob\_get\_status</span>返回最顶层输出缓冲区的状态信息；或者如果`full_status`设为**`TRUE`**，返回所有有效的输出缓冲级别。

### 参数

`full_status`  
设为**`TRUE`** 返回所有有效的输出缓冲区级别的状态信息。如果设为
**`FALSE`** 或者没有设置，仅返回最 顶层输出缓冲区的状态信息。

### 返回值

如果调用时没有`full_status`参数，或者`full_status` = **`FALSE`**
将返回一个包含下面元素的简单数组：

``` returnvalues
Array
(
    [level] => 2
    [type] => 0
    [status] => 0
    [name] => URL-Rewriter
    [del] => 1
)
```

| Key    | Value                                                                                                           |
|--------|-----------------------------------------------------------------------------------------------------------------|
| level  | 输出嵌套级别                                                                                                    |
| type   | *PHP\_OUTPUT\_HANDLER\_INTERNAL (0)* 或者 *PHP\_OUTPUT\_HANDLER\_USER (1)*                                      |
| status | *PHP\_OUTPUT\_HANDLER\_START* (0), *PHP\_OUTPUT\_HANDLER\_CONT* (1) or *PHP\_OUTPUT\_HANDLER\_END* (2) 三个之一 |
| name   | 起作用的输出处理程序的名字，或者是默认的输出处理程序的名字（如果没有设置的话）                                  |
| del    | 由<span class="function">ob\_start</span>设置的删除标签（Erase-flag）                                           |

如果调用时`full_status` =
**`TRUE`**，将返回一个数组，该数组的每个元素包含有效的输出缓冲区级别的状态信息。缓冲区的级别数用来当作数组的第一维数；每个元素自身是另一个数组，它持有该有效输出级别的状态信息。

    Array
    (
        [0] => Array
            (
                [chunk_size] => 0
                [size] => 40960
                [block_size] => 10240
                [type] => 1
                [status] => 0
                [name] => default output handler
                [del] => 1
            )

        [1] => Array
            (
                [chunk_size] => 0
                [size] => 40960
                [block_size] => 10240
                [type] => 0
                [buffer_size] => 0
                [status] => 0
                [name] => URL-Rewriter
                [del] => 1
            )

    )

完整的输出包含以下附加元素：

| Key         | Value                                                        |
|-------------|--------------------------------------------------------------|
| chunk\_size | 由 <span class="function">ob\_start</span>设置的Chunk size值 |
| size        | ...                                                          |
| blocksize   | ...                                                          |

### 参见

-   <span class="function">ob\_get\_level</span>
-   <span class="function">ob\_list\_handlers</span>

ob\_gzhandler
=============

在ob\_start中使用的用来压缩输出缓冲区中内容的回调函数。ob\_start
callback function to gzip output buffer

### 说明

<span class="type">string</span> <span
class="methodname">ob\_gzhandler</span> ( <span
class="methodparam"><span class="type">string</span> `$buffer`</span> ,
<span class="methodparam"><span class="type">int</span> `$mode`</span> )

<span class="function">ob\_gzhandler</span>目的是用在<span
class="function">ob\_start</span>中作回调函数，以方便将gz
编码的数据发送到支持压缩页面的浏览器。在<span
class="function">ob\_gzhandler</span>真正发送压缩过的数据之前，该
函数会确定（判定）浏览器可以接受哪种类型内容编码（"gzip","deflate",或者根本什么都不支持），然后
返回相应的输出。
所有可以发送正确头信息表明他自己可以接受压缩的网页的浏览器，都可以支持。
All browsers are supported since it's up to the browser to send the
correct header saying that it accepts compressed web pages.
如果一个浏览器不支持压缩过的页面，此函数返回**`FALSE`**。

### 参数

`buffer`  

`mode`  

### 返回值

### 更新日志

| 版本  | 说明                 |
|-------|----------------------|
| 4.0.5 | 填加了 `mode` 参数。 |

### 范例

**示例 \#1 <span class="function">ob\_gzhandler</span> example**

``` php
<?php

ob_start("ob_gzhandler");

?>
<html>
<body>
<p>This should be a compressed page.</p>
</html>
<body>
```

### 注释

> **Note**:
>
> <span class="function">ob\_gzhandler</span> 需要
> <a href="/ref/zlib.html" class="link">zlib</a> 扩展。

> **Note**:
>
> 不能同时使用<span class="function">ob\_gzhandler</span> 和
> <a href="/zlib/setup.html#" class="link">zlib.output_compression</a>。
> 也要注意使用
> <a href="/zlib/setup.html#" class="link">zlib.output_compression</a>
> 要优于 <span class="function">ob\_gzhandler</span>。

### 参见

-   <span class="function">ob\_start</span>
-   <span class="function">ob\_end\_flush</span>

ob\_implicit\_flush
===================

打开/关闭绝对刷送

### 说明

<span class="type">void</span> <span
class="methodname">ob\_implicit\_flush</span> (\[ <span
class="methodparam"><span class="type">int</span> `$flag`<span
class="initializer"> = true</span></span> \] )

<span
class="function">ob\_implicit\_flush</span>将打开或关闭绝对（隐式）刷送。绝对（隐式）刷送将导致在每次输出调用后有一次刷送操作，以便不再需要对
<span class="function">flush</span> 的显式调用。

### 参数

`flag`  
设为**`TRUE`** 打开绝对刷送，反之是 **`FALSE`** 。

### 返回值

没有返回值。

### 参见

-   <span class="function">flush</span>
-   <span class="function">ob\_start</span>
-   <span class="function">ob\_end\_flush</span>

ob\_list\_handlers
==================

列出所有使用中的输出处理程序。

### 说明

<span class="type">array</span> <span
class="methodname">ob\_list\_handlers</span> ( <span
class="methodparam">void</span> )

列出所有使用中的输出处理程序。

### 返回值

此函数将返回一个数组，数组元素是正在使用中输出处理程序名（如果存在的输出处理程序的话）。
如果启用了<a href="/outcontrol/setup.html#" class="link">output_buffering</a>
或者在 <span class="function">ob\_start</span>
中创建了一个匿名函数，<span class="function">ob\_list\_handlers</span>
将返回 "default output handler"。

### 范例

**示例 \#1 <span class="function">ob\_list\_handlers</span> example**

``` php
<?php
//using output_buffering=On
print_r(ob_list_handlers());
ob_end_flush();

ob_start("ob_gzhandler");
print_r(ob_list_handlers());
ob_end_flush();

// anonymous functions
ob_start(create_function('$string', 'return $string;'));
print_r(ob_list_handlers());
ob_end_flush();
?>
```

以上例程会输出：

    Array
    (
        [0] => default output handler
    )

    Array
    (
        [0] => ob_gzhandler
    )

    Array
    (
        [0] => default output handler
    )

### 参见

-   <span class="function">ob\_end\_clean</span>
-   <span class="function">ob\_end\_flush</span>
-   <span class="function">ob\_get\_flush</span>
-   <span class="function">ob\_start</span>

ob\_start
=========

打开输出控制缓冲

### 说明

<span class="type">bool</span> <span class="methodname">ob\_start</span>
(\[ <span class="methodparam"><span class="type">callback</span>
`$output_callback`</span> \[, <span class="methodparam"><span
class="type">int</span> `$chunk_size`</span> \[, <span
class="methodparam"><span class="type">bool</span> `$erase`</span>
\]\]\] )

此函数将打开输出缓冲。当输出缓冲激活后，脚本将不会输出内容（除http标头外），相反需要输出的内容被存储在内部缓冲区中。

内部缓冲区的内容可以用 <span class="function">ob\_get\_contents</span>
函数复制到一个字符串变量中。 想要输出存储在内部缓冲区中的内容，可以使用
<span class="function">ob\_end\_flush</span> 函数。另外， 使用 <span
class="function">ob\_end\_clean</span> 函数会静默丢弃掉缓冲区的内容。

**Warning**

当有正在调用的回调函数时，一些网络服务器（例如Apache）会改变一个脚本的工作目录。
你可以在回调函数中再把它改回来，例如
*chdir(dirname($\_SERVER\['SCRIPT\_FILENAME'\]))* 。

输出缓冲区是可堆叠的，这即意谓着，当有一个 <span
class="function">ob\_start</span> 是活跃的时， 你可以调用另一个 <span
class="function">ob\_start</span> 。 只要确保又正确调用了 <span
class="function">ob\_end\_flush</span> 恰当的次数即可。
如果有多重输出回调函数是活跃的，输出内容会一直按嵌套的顺序依次通过它们而被过滤。

### 参数

`output_callback`  
可选参数 `output_callback` 函数可以被指定。
此函数把一个字符串当作参数并返回一个字符串。 当输出缓冲区被( <span
class="function">ob\_flush</span>, <span
class="function">ob\_clean</span>
或者相似的函数)冲刷（送出）或者被清洗的时候；或者在请求结束之际输出缓冲区内容被冲刷到浏览器的时候该函数将会被调用。
当调用 `output_callback` 时，它将收到输出缓冲区的内容作为参数
并预期返回一个新的输出缓冲区作为结果，这个新返回的输出缓冲区内容将被送到浏览器。
如果这个 `output_callback` 不是一个可以调用的函数，此函数 会返回
**`FALSE`** 。

如果回调函数有两个参数，第二个参数会由一个位域补充，该位域由
**`PHP_OUTPUT_HANDLER_START`**, **`PHP_OUTPUT_HANDLER_CONT`** 和
**`PHP_OUTPUT_HANDLER_END`** 组成。

如果 `output_callback` 返回 **`FALSE`** ，其原来的输入
内容被直接送到浏览器。

这个参数 `output_callback` 可以通过直接给一个 **`NULL`** 值而避开。

<span class="function">ob\_end\_clean</span>, <span
class="function">ob\_end\_flush</span>, <span
class="function">ob\_clean</span>, <span
class="function">ob\_flush</span> and <span
class="function">ob\_start</span> 不能从一个回调函数中调用。
如果从回调函数中调用了它们，产生的行为是不明确的。
如果想要删除缓冲区的内容，从回调函数中返回一个"" (空字符串)。
更不能从一个回调函数中使用像*print\_r($expression, true)*
或*highlight\_file($filename, true)* 一样的输出缓冲函数。

> **Note**:
>
> 在PHP 4.0.4中， <span class="function">ob\_gzhandler</span>
> 被引入是为了简化把gz编码过 数据发送到支持压缩网页的浏览器。 <span
> class="function">ob\_gzhandler</span>
> 会判定浏览器可以接受哪种类型的编码内容，并返回相应 的输出。

`chunk_size`  
如果可选参数 `chunk_size` 被赋值了，在任何一个能引起缓冲区的长度等于
或超过 `chunk_size` 的输出操作后，缓冲区都会被刷送。 默认值 0
意味着函数仅在最后被调用，其余的特殊值可以将 `chunk_size` 从 1 设定到
4096。

`erase`  
如果可选参数 `erase` 被赋成
**`FALSE`**，直到脚本执行完成缓冲区才被删除。
这使得，如果调用了冲刷和清洗（清除）函数，会抛出一个“notice”,并返回
**`FALSE`** 值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 更新日志

| 版本  | 说明                                                                   |
|-------|------------------------------------------------------------------------|
| 4.3.2 | 在传递的 `output_callback` 不能被执行时，此函数 被改成返回 **`FALSE`** |
| 4.2.0 | 添加了 `erase` 参数。                                                  |

### 范例

**示例 \#1 用户自定义回调函数的例子**

``` php
<?php

function callback($buffer)
{
  // replace all the apples with oranges
  return (str_replace("apples", "oranges", $buffer));
}

ob_start("callback");

?>
<html>
<body>
<p>It's like comparing apples to oranges.</p>
</body>
</html>
<?php

ob_end_flush();

?>
```

以上例程会输出：

    <html>
    <body>
    <p>It's like comparing oranges to oranges.</p>
    </body>
    </html>

### 参见

-   <span class="function">ob\_get\_contents</span>
-   <span class="function">ob\_end\_clean</span>
-   <span class="function">ob\_end\_flush</span>
-   <span class="function">ob\_implicit\_flush</span>
-   <span class="function">ob\_gzhandler</span>
-   <span class="function">ob\_iconv\_handler</span>
-   <span class="function">mb\_output\_handler</span>
-   <span class="function">ob\_tidyhandler</span>

output\_add\_rewrite\_var
=========================

添加URL重写器的值（Add URL rewriter values）

### 说明

<span class="type">bool</span> <span
class="methodname">output\_add\_rewrite\_var</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> ,
<span class="methodparam"><span class="type">string</span>
`$value`</span> )

此函数给URL重写机制添加名/值对。
这种名值对将被添加到URL（以GET参数的形式）和表单（以input隐藏域的形式），当透明URL重写用
<a href="/session/setup.html#" class="link">session.use_trans_sid</a>
开启时同样可以添加到session ID。
要注意，绝对URL(http://example.com/..)不能被重写。

此函数的行为由<a href="/session/setup.html#" class="link">url_rewriter.tags</a>
`php.ini` 参数控制。

> **Note**: <span class="simpara">
> 如果还没有活跃的输出缓冲区，调用此函数将隐式地开启它。 </span>

### 参数

`name`  
变量名。

`value`  
变量值。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">output\_add\_rewrite\_var</span>
example**

``` php
<?php
output_add_rewrite_var('var', 'value');

// some links
echo '<a href="file.php">link</a>
<a href="http://example.com">link2</a>';

// a form
echo '<form action="script.php" method="post">
<input type="text" name="var2" />
</form>';

print_r(ob_list_handlers());
?>
```

以上例程会输出：

    <a href="file.php?var=value">link</a>
    <a href="http://example.com">link2</a>

    <form action="script.php" method="post">
    <input type="hidden" name="var" value="value" />
    <input type="text" name="var2" />
    </form>

    Array
    (
        [0] => URL-Rewriter
    )

### 参见

-   <span class="function">output\_reset\_rewrite\_vars</span>
-   <span class="function">ob\_flush</span>
-   <span class="function">ob\_list\_handlers</span>

output\_reset\_rewrite\_vars
============================

重设URL重写器的值（Reset URL rewriter values）

### 说明

<span class="type">bool</span> <span
class="methodname">output\_reset\_rewrite\_vars</span> ( <span
class="methodparam">void</span> )

此函数重置URL重写器，移除所有的先前由 <span
class="function">output\_add\_rewrite\_var</span>
函数设置的重写变量，或者移除会话机制（如果*session.use\_trans\_sid* 在
<span class="function">session\_start</span>上进行了设置）。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">output\_reset\_rewrite\_vars</span>
example**

``` php
<?php
session_start();
output_add_rewrite_var('var', 'value');

echo '<a href="file.php">link</a>';
ob_flush();

output_reset_rewrite_vars();
echo '<a href="file.php">link</a>';
?>
```

以上例程会输出：

    <a href="file.php?PHPSESSID=xxx&var=value">link</a>
    <a href="file.php">link</a>

### 参见

-   <span class="function">output\_add\_rewrite\_var</span>
-   <span class="function">ob\_flush</span>
-   <span class="function">ob\_list\_handlers</span>
-   <span class="function">session\_start</span>

**目录**

-   [flush](/ref/outcontrol.html#flush) — 刷新输出缓冲
-   [ob\_clean](/ref/outcontrol.html#ob_clean) — 清空（擦掉）输出缓冲区
-   [ob\_end\_clean](/ref/outcontrol.html#ob_end_clean) —
    清空（擦除）缓冲区并关闭输出缓冲
-   [ob\_end\_flush](/ref/outcontrol.html#ob_end_flush) —
    冲刷出（送出）输出缓冲区内容并关闭缓冲
-   [ob\_flush](/ref/outcontrol.html#ob_flush) —
    冲刷出（送出）输出缓冲区中的内容
-   [ob\_get\_clean](/ref/outcontrol.html#ob_get_clean) —
    得到当前缓冲区的内容并删除当前输出缓。
-   [ob\_get\_contents](/ref/outcontrol.html#ob_get_contents) —
    返回输出缓冲区的内容
-   [ob\_get\_flush](/ref/outcontrol.html#ob_get_flush) —
    刷出（送出）缓冲区内容，以字符串形式返回内容，并关闭输出缓冲区。
-   [ob\_get\_length](/ref/outcontrol.html#ob_get_length) —
    返回输出缓冲区内容的长度
-   [ob\_get\_level](/ref/outcontrol.html#ob_get_level) —
    返回输出缓冲机制的嵌套级别
-   [ob\_get\_status](/ref/outcontrol.html#ob_get_status) —
    得到所有输出缓冲区的状态
-   [ob\_gzhandler](/ref/outcontrol.html#ob_gzhandler) —
    在ob\_start中使用的用来压缩输出缓冲区中内容的回调函数。ob\_start
    callback function to gzip output buffer
-   [ob\_implicit\_flush](/ref/outcontrol.html#ob_implicit_flush) —
    打开/关闭绝对刷送
-   [ob\_list\_handlers](/ref/outcontrol.html#ob_list_handlers) —
    列出所有使用中的输出处理程序。
-   [ob\_start](/ref/outcontrol.html#ob_start) — 打开输出控制缓冲
-   [output\_add\_rewrite\_var](/ref/outcontrol.html#output_add_rewrite_var)
    — 添加URL重写器的值（Add URL rewriter values）
-   [output\_reset\_rewrite\_vars](/ref/outcontrol.html#output_reset_rewrite_vars)
    — 重设URL重写器的值（Reset URL rewriter values）
