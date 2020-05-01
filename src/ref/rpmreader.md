rpm\_close
==========

Closes an RPM file

### 说明

<span class="type">bool</span> <span
class="methodname">rpm\_close</span> ( <span class="methodparam"><span
class="type">resource</span> `$rpmr`</span> )

<span class="function">rpm\_close</span> will close an RPM file pointer.

### 参数

`rpmr`  
A file pointer resource successfully opened by <span
class="function">rpm\_open</span>.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">rpm\_close</span> example**

``` php
<?php

$file = "/path/to/file.rpm";
$rpmr = rpm_open($file);

rpm_close($rpmr);

?>
```

### 参见

-   <span class="function">rpm\_open</span>

rpm\_get\_tag
=============

Retrieves a header tag from an RPM file

### 说明

<span class="type">mixed</span> <span
class="methodname">rpm\_get\_tag</span> ( <span
class="methodparam"><span class="type">resource</span> `$rpmr`</span> ,
<span class="methodparam"><span class="type">int</span> `$tagnum`</span>
)

<span class="function">rpm\_get\_tag</span> will retrieve a given tag
from the RPM file's header and return it.

### 参数

`rpmr`  
A file pointer resource successfully opened by <span
class="function">rpm\_open</span>.

`tagnum`  
The tag number to retrieve from the RPM header. This value can be
specified using the list of constants defined by this module.

### 返回值

The return value can be of various types depending on the `tagnum`
supplied to the function.

### 范例

**示例 \#1 <span class="function">rpm\_get\_tag</span> example**

``` php
<?php

$file = "/path/to/file.rpm";
$rpmr = rpm_open($file);

$name = rpm_get_tag($rpmr, RPMREADER_NAME);
echo "$name<br>\n";

rpm_close($rpmr);

?>
```

### 参见

-   <span class="function">rpm\_open</span>
-   <span class="function">rpm\_close</span>

rpm\_is\_valid
==============

Tests a filename for validity as an RPM file

### 说明

<span class="type">bool</span> <span
class="methodname">rpm\_is\_valid</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

<span class="function">rpm\_is\_valid</span> will test an RPM file for
validity as an RPM file. This is not the same as <span
class="function">rpm\_open</span> as it only checks the file for
validity but does not return a file pointer to be used by further
functions.

### 参数

`filename`  
The filename of the RPM file you wish to check for validity.

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

### 范例

**示例 \#1 <span class="function">rpm\_is\_valid</span> example**

``` php
<?php

$file = "/path/to/file.rpm";

if (rpm_is_valid($file)) {
    echo "File is recognized as an RPM file.<br>\n";
}
else {
    echo "File is not recognized as an RPM file.<br>\n";
}

?>
```

rpm\_open
=========

Opens an RPM file

### 说明

<span class="type">resource</span> <span
class="methodname">rpm\_open</span> ( <span class="methodparam"><span
class="type">string</span> `$filename`</span> )

<span class="function">rpm\_open</span> will open an RPM file and will
determine if the file is a valid RPM file.

### 参数

`filename`  
The filename of the RPM file you wish to open.

### 返回值

If the open succeeds, then <span class="function">rpm\_open</span> will
return a file pointer resource to the newly opened file. On error, the
function will return **`FALSE`**.

### 范例

**示例 \#1 <span class="function">rpm\_open</span> example**

``` php
<?php

$file = "/path/to/file.rpm";
$rpmr = rpm_open($file);

rpm_close($rpmr);

?>
```

### 参见

-   <span class="function">rpm\_close</span>

rpm\_version
============

Returns a string representing the current version of the rpmreader
extension

### 说明

<span class="type">string</span> <span
class="methodname">rpm\_version</span> ( <span
class="methodparam">void</span> )

<span class="function">rpm\_version</span> will return the current
version of the rpmreader extension.

### 返回值

<span class="function">rpm\_version</span> will return a string
representing the rpmreader version currently loaded in PHP.

### 范例

**示例 \#1 <span class="function">rpm\_version</span> example**

``` php
<?php

$rpmr_ver = rpm_version();

echo "$rpmr_ver<br />\n";

?>
```

**目录**

-   [rpm\_close](/ref/rpmreader.html#rpm_close) — Closes an RPM file
-   [rpm\_get\_tag](/ref/rpmreader.html#rpm_get_tag) — Retrieves a
    header tag from an RPM file
-   [rpm\_is\_valid](/ref/rpmreader.html#rpm_is_valid) — Tests a
    filename for validity as an RPM file
-   [rpm\_open](/ref/rpmreader.html#rpm_open) — Opens an RPM file
-   [rpm\_version](/ref/rpmreader.html#rpm_version) — Returns a string
    representing the current version of the rpmreader extension
