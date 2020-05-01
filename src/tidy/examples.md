范例
====

**目录**

-   [Tidy example](/tidy/examples.html#Tidy%20example)

Tidy example
------------

This simple example shows basic Tidy usage.

**示例 \#1 Basic Tidy usage**

``` php
<?php
ob_start();
?>
<html>a html document</html>
<?php
$html = ob_get_clean();

// Specify configuration
$config = array(
           'indent'         => true,
           'output-xhtml'   => true,
           'wrap'           => 200);

// Tidy
$tidy = new tidy;
$tidy->parseString($html, $config, 'utf8');
$tidy->cleanRepair();

// Output
echo $tidy;
?>
```
