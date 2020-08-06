Error::\_\_toString
===================

error 的字符串表达

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

返回 Error 的 <span class="type">string</span>表达形式。

### 参数

此函数没有参数。

### 返回值

返回 Error 的 <span class="type">string</span>表达形式。

### 范例

**示例 \#1 <span class="function">Error::\_\_toString</span> 例子**

``` php
<?php
try {
    throw new Error("Some error message");
} catch(Error $e) {
    echo $e;
}
?>
```

以上例程的输出类似于：

    Error: Some error message in /home/bjori/tmp/ex.php:3
    Stack trace:
    #0 {main}

### 参见

-   <span class="methodname">Throwable::\_\_toString</span>
