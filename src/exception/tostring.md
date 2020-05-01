Exception::\_\_toString
=======================

将异常对象转换为字符串

### 说明

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

返回转换为字符串（<span class="type">string</span>）类型的异常。

### 参数

此函数没有参数。

### 返回值

返回转换为字符串（<span class="type">string</span>）类型的异常。

### 范例

**示例 \#1 <span class="function">Exception::\_\_toString</span>示例**

``` php
<?php
try {
    throw new Exception("Some error message");
} catch(Exception $e) {
    echo $e;
}
?>
```

以上例程的输出类似于：

    exception 'Exception' with message 'Some error message' in /home/bjori/tmp/ex.php:3
    Stack trace:
    #0 {main}

### 参见

-   <span class="methodname">Throwable::\_\_toString</span>
