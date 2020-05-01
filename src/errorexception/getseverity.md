ErrorException::getSeverity
===========================

获取异常的严重程度

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">ErrorException::getSeverity</span> ( <span
class="methodparam">void</span> )

返回异常的严重程度。

### 参数

此函数没有参数。

### 返回值

返回异常的严重级别。

### 范例

**示例 \#1 <span class="function">ErrorException::getSeverity</span>
例子**

``` php
<?php
try {
    throw new ErrorException("Exception message", 0, E_USER_ERROR);
} catch(ErrorException $e) {
    echo "This exception severity is: " . $e->getSeverity();
    var_dump($e->getSeverity() === E_USER_ERROR);
}
?>
```

以上例程的输出类似于：

    This exception severity is: 256
    bool(true)
