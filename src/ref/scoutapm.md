scoutapm\_get\_calls
====================

Returns a list of instrumented calls that have occurred

### 说明

<span class="type">array</span> <span
class="methodname">scoutapm\_get\_calls</span> ( <span
class="methodparam">void</span> )

Returns a list of any instrumented function calls since <span
class="function">scoutapm\_get\_calls</span> was last called. The list
is cleared each time the function is called.

### 参数

此函数没有参数。

### 返回值

<span class="function">scoutapm\_get\_calls</span> returns an array
containing a list of all recorded calls to instrumented function calls.

### 范例

**示例 \#1 Fetch instrumented calls**

``` php
<?php

file_get_contents('a.txt');
file_get_contents('b.txt');

print_r(scoutapm_get_calls());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => Array
            (
                [function] => file_get_contents
                [entered] => 1576839727.7934
                [exited] => 1576839727.7935
                [time_taken] => 2.7894973754883E-5
                [argv] => Array
                    (
                        [0] => a.txt
                    )

            )

        [1] => Array
            (
                [function] => file_get_contents
                [entered] => 1576839727.7935
                [exited] => 1576839727.7935
                [time_taken] => 7.8678131103516E-6
                [argv] => Array
                    (
                        [0] => b.txt
                    )

            )

    )

scoutapm\_list\_instrumented\_functions
=======================================

List functions scoutapm will instrument.

### 说明

<span class="type">array</span> <span
class="methodname">scoutapm\_list\_instrumented\_functions</span> (
<span class="methodparam">void</span> )

Returns a list of the functions the extension will instrument.

### 参数

此函数没有参数。

### 返回值

<span class="function">scoutapm\_list\_instrumented\_functions</span>
returns an array containing a list of all functions that the scoutapm
extension is able to instrument in the current installation.

### 范例

**示例 \#1 Fetch the list of functions scoutapm will instrument**

``` php
<?php
print_r(scoutapm_list_instrumented_functions());
?>
```

以上例程的输出类似于：

    Array
    (
        [0] => file_get_contents
        [1] => file_put_contents
        [2] => fopen
        [3] => fread
        [4] => fwrite
        [5] => pdo->exec
        [6] => pdo->query
        [7] => pdo->prepare
        [8] => pdostatement->execute
    )

**目录**

-   [scoutapm\_get\_calls](/ref/scoutapm.html#scoutapm_get_calls) —
    Returns a list of instrumented calls that have occurred
-   [scoutapm\_list\_instrumented\_functions](/ref/scoutapm.html#scoutapm_list_instrumented_functions)
    — List functions scoutapm will instrument.
