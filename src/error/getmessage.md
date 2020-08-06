Error::getMessage
=================

获取错误信息

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

返回错误信息。

### 参数

此函数没有参数。

### 返回值

返回字符串错误信息。

### 范例

**示例 \#1 <span class="function">Error::getMessage</span> 例子**

``` php
<?php
try {
    throw new Error("Some error message");
} catch(Error $e) {
    echo $e->getMessage();
}
?>
```

以上例程的输出类似于：

    Some error message

### 参见

-   <span class="methodname">Throwable::getMessage</span>
