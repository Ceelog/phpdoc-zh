范例
====

**目录**

-   [Example that shows the effect of
    scream](/scream/examples.html#Example%20that%20shows%20the%20effect%20of%20scream)

Example that shows the effect of scream
---------------------------------------

This example demonstrates how scream affects the behaviour of PHP's
error handler.

**示例 \#1 Enabling and disabling scream at runtime**

``` php
<?php
// Make sure errors will be shown
ini_set('display_errors', true);
error_reporting(E_ALL);

// Disable scream - this is the default and produce an error
ini_set('scream.enabled', false);
echo "Opening http://example.com/not-existing-file\n";
@fopen('http://example.com/not-existing-file', 'r');

// Now enable scream and try again
ini_set('scream.enabled', true);
echo "Opening http://example.com/not-existing-file\n";
@fopen('http://example.com/not-existing-file', 'r');
?>
```

以上例程的输出类似于：

    Opening http://example.com/not-existing-file
    Opening http://example.com/not-existing-file

    Warning: fopen(http://example.com/not-existing-file): failed to open stream: HTTP request failed! HTTP/1.1 404 Not Found in example.php on line 14

> **Note**: <span class="simpara"> Usually one would set this in the
> <a href="/configuration/file.html" class="link">php.ini configuration file</a>
> instead of changing the code. </span>
