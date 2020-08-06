Error::getTraceAsString
=======================

获取字符串形式的调用栈（stack trace）

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

以字符串形式返回 stack trace。

### 参数

此函数没有参数。

### 返回值

以字符串形式返回 stack trace。

### 范例

**示例 \#1 <span class="function">Error::getTraceAsString</span> 例子**

``` php
<?php
function test() {
    throw new Error;
}

try {
    test();
} catch(Error $e) {
    echo $e->getTraceAsString();
}
?>
```

以上例程的输出类似于：

    #0 /home/bjori/tmp/ex.php(7): test()
    #1 {main}

### 参见

-   <span class="methodname">Throwable::getTraceAsString</span>
