Exception::getLine
==================

获取创建的异常所在文件中的行号

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

返回发生异常的代码在文件中的行号。

### 参数

此函数没有参数。

### 返回值

返回发生异常的代码在文件中的行号。

### 范例

**示例 \#1 <span class="function">Exception::getLine</span>示例**

``` php
<?php
try {
    throw new Exception("Some error message");
} catch(Exception $e) {
    echo "The exception was thrown on line: " . $e->getLine();
}
?>
```

以上例程的输出类似于：

    The exception was thrown on line: 3

### 参见

-   <span class="methodname">Throwable::getLine</span>
