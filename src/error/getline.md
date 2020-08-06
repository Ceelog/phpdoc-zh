Error::getLine
==============

获取错误发生时的行号

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

获取错误发生时的行号。

### 参数

此函数没有参数。

### 返回值

返回错误发生时的行号。

### 范例

**示例 \#1 <span class="function">Error::getLine</span> 例子**

``` php
<?php
try {
    throw new Error("Some error message");
} catch(Error $e) {
    echo "The error was created on line: " . $e->getLine();
}
?>
```

以上例程的输出类似于：

    The error was created on line: 3

### 参见

-   <span class="methodname">Throwable::getLine</span>
