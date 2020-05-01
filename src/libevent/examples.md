范例
====

**示例 \#1 polling **`STDIN`** using basic API**

``` php
<?php

function print_line($fd, $events, $arg)
{
    static $max_requests = 0;

    $max_requests++;

    if ($max_requests == 10) {
        // exit loop after 10 writes
        event_base_loopexit($arg[1]);
    }

    // print the line
    echo  fgets($fd);
}

// create base and event
$base = event_base_new();
$event = event_new();

$fd = STDIN;

// set event flags
event_set($event, $fd, EV_READ | EV_PERSIST, "print_line", array($event, $base));
// set event base
event_base_set($event, $base);

// enable event
event_add($event);
// start event loop
event_base_loop($base);

?>
```

**示例 \#2 polling **`STDIN`** using buffered event API**

``` php
<?php

function print_line($buf, $arg)
{
    static $max_requests;

    $max_requests++;

    if ($max_requests == 10) {
        event_base_loopexit($arg);
    }

    // print the line
    echo event_buffer_read($buf, 4096);
}

function error_func($buf, $what, $arg)
{
    // handle errors
}

$base = event_base_new();
$eb = event_buffer_new(STDIN, "print_line", NULL, "error_func", $base);

event_buffer_base_set($eb, $base);
event_buffer_enable($eb, EV_READ);

event_base_loop($base);

?>
```
