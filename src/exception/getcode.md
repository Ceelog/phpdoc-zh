Exception::getCode
==================

获取异常代码

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

返回异常代码。

### 参数

此函数没有参数。

### 返回值

<span class="classname">Exception</span> 返回整型（<span
class="type">int</span>）的异常代码，但在其他类中可能返回其他类型(比如在
<span class="classname">PDOException</span> 中返回 <span
class="type">string</span>)。

### 范例

**示例 \#1 <span class="function">Exception::getCode</span>示例**

``` php
<?php
try {
    throw new Exception("Some error message", 30);
} catch(Exception $e) {
    echo "The exception code is: " . $e->getCode();
}
?>
```

以上例程的输出类似于：

    The exception code is: 30

### 参见

-   <span class="methodname">Throwable::getCode</span>
