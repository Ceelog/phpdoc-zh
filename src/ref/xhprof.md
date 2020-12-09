xhprof\_disable
===============

停止 xhprof 分析器

### 说明

<span class="type">array</span> <span
class="methodname">xhprof\_disable</span> ( <span
class="methodparam">void</span> )

停止性能分析，并返回此次运行的 xhprof 数据。

### 参数

此函数没有参数。

### 返回值

本次运行的 <span class="type">array</span> 类型的 xhprof 数据。

### 范例

**示例 \#1 <span class="function">xhprof\_disable</span> 范例**

``` php
<?php
xhprof_enable();

$foo = strlen("foo bar");

$xhprof_data = xhprof_disable();

print_r($xhprof_data);
?>
```

以上例程的输出类似于：

    Array
    (
        [main()==>strlen] => Array
            (
                [ct] => 1
                [wt] => 279
            )

        [main()==>xhprof_disable] => Array
            (
                [ct] => 1
                [wt] => 9
            )

        [main()] => Array
            (
                [ct] => 1
                [wt] => 610
            )

    )

xhprof\_enable
==============

启动 xhprof 性能分析器

### 说明

<span class="type">void</span> <span
class="methodname">xhprof\_enable</span> (\[ <span
class="methodparam"><span class="type">int</span> `$flags`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">array</span> `$options`</span>
\]\] )

启动 xhprof 进行性能分析。

### 参数

`flags`  
分析添加额外信息的可选标记。 关于此标记的更多信息参见
<a href="/xhprof/constants.html" class="link">XHprof 常量</a>，例如，
**`XHPROF_FLAGS_MEMORY`** 可以开启内存的分析。

`options`  
<span class="type">array</span> 的可选选项，就是通过传递
'ignored\_functions' 选项来忽略性能分析中的某些函数。

### 返回值

**`null`**

### 更新日志

| 版本  | 说明                        |
|-------|-----------------------------|
| 0.9.2 | 添加可选的 `options` 参数。 |

### 范例

**示例 \#1 <span class="function">xhprof\_enable</span> 范例**

``` php
<?php
// 1. elapsed time + memory + CPU profiling; and ignore built-in (internal) functions
xhprof_enable(XHPROF_FLAGS_NO_BUILTINS | XHPROF_FLAGS_CPU | XHPROF_FLAGS_MEMORY);

// 2. elapsed time profiling; ignore call_user_func* during profiling
xhprof_enable(
    0,
    array('ignored_functions' =>  array('call_user_func',
                                        'call_user_func_array')));
                                       
// 3. elapsed time + memory profiling; ignore call_user_func* during profiling
xhprof_enable(
    XHPROF_FLAGS_MEMORY,
    array('ignored_functions' =>  array('call_user_func',
                                        'call_user_func_array')));
?>
```

### 参见

-   <span class="function">xhprof\_disable</span>
-   <span class="function">xhprof\_sample\_enable</span>
-   <span class="function">memory\_get\_usage</span>
-   <span class="function">getrusage</span>

xhprof\_sample\_disable
=======================

停止 xhprof 性能采样分析器

### 说明

<span class="type">array</span> <span
class="methodname">xhprof\_sample\_disable</span> ( <span
class="methodparam">void</span> )

停止采样模式的 xhprof 分析器。

### 参数

此函数没有参数。

### 返回值

本次运行的xhprof采样数据，<span class="type">array</span> 类型。

### 范例

**示例 \#1 <span class="function">xhprof\_sample\_disable</span> 范例**

``` php
<?php
xhprof_sample_enable();

for ($i = 0; $i <= 10000; $i++) {
    $a = strlen($i);
    $b = $i * $a;
    $c = rand();
}

$xhprof_data = xhprof_sample_disable();

print_r($xhprof_data);
?>
```

以上例程的输出类似于：

    Array
    (
        [1272935300.800000] => main()
        [1272935300.900000] => main()
    )

xhprof\_sample\_enable
======================

以采样模式启动 XHProf 性能分析

### 说明

<span class="type">void</span> <span
class="methodname">xhprof\_sample\_enable</span> ( <span
class="methodparam">void</span> )

<span class="function">xhprof\_enable</span>
的更轻量的版本，以采样模式开始性能分析。 抽样的间隔为 0.1
秒，样本记录了完整的函数调用堆栈。
主要使用的情况是以较低的性能开销来进行性能监控和诊断。

### 参数

此函数没有参数。

### 返回值

**`null`**

### 参见

-   <span class="function">xhprof\_sample\_disable</span>
-   <span class="function">xhprof\_enable</span>
-   <span class="function">memory\_get\_usage</span>
-   <span class="function">getrusage</span>

**目录**

-   [xhprof\_disable](/ref/xhprof.html#xhprof_disable) — 停止 xhprof
    分析器
-   [xhprof\_enable](/ref/xhprof.html#xhprof_enable) — 启动 xhprof
    性能分析器
-   [xhprof\_sample\_disable](/ref/xhprof.html#xhprof_sample_disable) —
    停止 xhprof 性能采样分析器
-   [xhprof\_sample\_enable](/ref/xhprof.html#xhprof_sample_enable) —
    以采样模式启动 XHProf 性能分析
