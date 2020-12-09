stomp\_connect\_error
=====================

Returns a string description of the last connect error

### 说明

<span class="type">string</span> <span
class="methodname">stomp\_connect\_error</span> ( <span
class="methodparam">void</span> )

Returns a string description of the last connect error.

### 参数

此函数没有参数。

### 返回值

A string that describes the error, or **`null`** if no error occurred.

### 范例

**示例 \#1 <span class="function">stomp\_connect\_error</span> example**

``` php
<?php
$link = stomp_connect('http://localhost:61613');

if(!$link) {
    die('Connection failed: ' . stomp_connect_error());
}
?>
```

以上例程的输出类似于：

    Connection failed: Invalid Broker URI scheme

stomp\_version
==============

Gets the current stomp extension version

### 说明

<span class="type">string</span> <span
class="methodname">stomp\_version</span> ( <span
class="methodparam">void</span> )

Returns a string containing the version of the current stomp extension.

### 参数

此函数没有参数。

### 返回值

It returns the current stomp extension version

### 范例

**示例 \#1 <span class="function">stomp\_version</span> example**

``` php
<?php

var_dump(stomp_version());

?>
```

以上例程的输出类似于：

    string(5) "0.2.0"

**目录**

-   [stomp\_connect\_error](/ref/stomp.html#stomp_connect_error) —
    Returns a string description of the last connect error
-   [stomp\_version](/ref/stomp.html#stomp_version) — Gets the current
    stomp extension version
