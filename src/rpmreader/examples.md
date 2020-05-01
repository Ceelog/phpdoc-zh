范例
====

**目录**

-   [Basic usage](/rpmreader/examples.html#Basic%20usage)

Basic usage
-----------

This example will open an RPM file and read the name, version, and
release from the RPM file, echo the results, and close the RPM file.

**示例 \#1 Basic RPMReader Example**

``` php
<?php

$filename = "/path/to/file.rpm";

// open file
$rpmr = rpm_open($filename);

// get "Name" tag
$name = rpm_get_tag($rpmr, RPMREADER_NAME);

// get "Version" tag
$ver = rpm_get_tag($rpmr, RPMREADER_VERSION);

// get "Release" tag
$rel = rpm_get_tag($rpmr, RPMREADER_RELEASE);

echo "$name-$ver-$rel<br>\n";

// close file
rpm_close($rpmr);

?>
```
