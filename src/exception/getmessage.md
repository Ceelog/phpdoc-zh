Exception::getMessage
=====================

获取异常消息内容

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

返回异常消息内容。

### 参数

此函数没有参数。

### 返回值

返回字符串类型的异常消息内容。

### 范例

**示例 \#1 <span class="function">Exception::getMessage</span>示例**

``` php
<?php
try {
    throw new Exception("Some error message");
} catch(Exception $e) {
    echo $e->getMessage();
}
?>
```

以上例程的输出类似于：

    Some error message

### 参见

-   <span class="methodname">Throwable::getMessage</span>
