Exception::getTraceAsString
===========================

获取字符串类型的异常追踪信息

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

以字符串类型返回异常追踪信息。

### 参数

此函数没有参数。

### 返回值

以字符串类型返回异常追踪信息。

### 范例

**示例 \#1 <span
class="function">Exception::getTraceAsString</span>示例**

``` php
<?php
function test() {
    throw new Exception;
}

try {
    test();
} catch(Exception $e) {
    echo $e->getTraceAsString();
}
?>
```

以上例程的输出类似于：

    #0 /home/bjori/tmp/ex.php(7): test()
    #1 {main}

### 参见

-   <span class="methodname">Throwable::getTraceAsString</span>
