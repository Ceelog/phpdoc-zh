范例
====

**目录**

-   [Basic usage](/hrtime/examples.html#Basic%20usage)

Basic usage
-----------

The example illustrates the basic StopWatch class usage

**示例 \#1 Measure several code blocks execution and get the total**

``` php
<?php

$c = new HRTime\StopWatch;

$c->start();
/* measure this code block execution */
for ($i = 0; $i < 1024*1024; $i++);
$c->stop();
$elapsed0 = $c->getLastElapsedTime(HRTime\Unit::NANOSECOND);

/* measurement is not running here*/
for ($i = 0; $i < 1024*1024; $i++);

$c->start();
/* measure this code block execution */
for ($i = 0; $i < 1024*1024; $i++);
$c->stop();
$elapsed1 = $c->getLastElapsedTime(HRTime\Unit::NANOSECOND);

$elapsed_total = $c->getElapsedTime(HRTime\Unit::NANOSECOND);

?>
```
