范例
====

**目录**

-   [Basic usage](/memtrack/examples.html#Basic%20usage)

Basic usage
-----------

Basic example on using memtrack extension:

**示例 \#1 Creating large array in a function**

``` php
<?php

/* /tmp/example1.php */

function foo() {
    $a = array();
    for ($i = 0; $i < 10000; $i++) $a[] = "test";
    return $a;
}
$arr = foo();

?>
```

Run the example with the following command:

    php -d memtrack.enabled=1 -d memtrack.soft_limit=1M -d memtrack.vm_limit=3M /tmp/example1.php

以上例程的输出类似于：

    Warning: [memtrack] [pid 26177] user function foo() executed in /tmp/example1.php on line 10 allocated 4194304 bytes in /tmp/example1.php on line 0
    Warning: [memtrack] [pid 26177] virtual memory usage on shutdown: 32911360 bytes in Unknown on line 0
