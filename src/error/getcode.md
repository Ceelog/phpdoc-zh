Error::getCode
==============

获取错误代码

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

返回错误代码。

### 参数

此函数没有参数。

### 返回值

返回 <span class="type">integer</span> 的错误代码

### 范例

**示例 \#1 <span class="function">Error::getCode</span> 例子**

``` php
<?php
try {
    throw new Error("Some error message", 30);
} catch(Error $e) {
    echo "The Error code is: " . $e->getCode();
}
?>
```

以上例程的输出类似于：

    The Error code is: 30

### 参见

-   <span class="methodname">Throwable::getCode</span>
