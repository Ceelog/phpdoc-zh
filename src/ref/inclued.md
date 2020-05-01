inclued\_get\_data
==================

Get the inclued data

### 说明

<span class="type">array</span> <span
class="methodname">inclued\_get\_data</span> ( <span
class="methodparam">void</span> )

Get the inclued data.

### 参数

此函数没有参数。

### 返回值

The inclued data.

### 范例

**示例 \#1 <span class="function">inclued\_get\_data</span> example**

See the
<a href="/inclued/examples.html#Example%20that%20implements%20inclued%20into%20an%20application" class="link">inclued examples</a>
section for ways to create graphs with this data.

``` php
<?php 
include 'x.php';

$clue = inclued_get_data();

print_r($clue);
?>
```

以上例程的输出类似于：

    Array
    (
      [includes] => Array
        (
          [0] => Array
            (
              [operation] => include
              [op_type] => 2
              [filename] => x.php
              [opened_path] => /tmp/x.php
              [fromfile] => /tmp/z.php
              [fromline] => 2
            )
        )
    )

### 参见

-   <a href="/inclued/examples.html#Example%20that%20implements%20inclued%20into%20an%20application" class="link">inclued examples</a>
-   <span class="function">debug\_backtrace</span>
-   <span class="function">include</span>

**目录**

-   [inclued\_get\_data](/ref/inclued.html#inclued_get_data) — Get the
    inclued data
