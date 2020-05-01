Exception::getFile
==================

创建异常时的程序文件名称

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

获取创建异常的程序文件名称。

### 参数

此函数没有参数。

### 返回值

返回发生异常的程序文件名称。

### 范例

**示例 \#1 <span class="function">Exception::getFile</span>示例**

``` php
<?php
try {
    throw new Exception;
} catch(Exception $e) {
    echo $e->getFile();
}
?>
```

以上例程的输出类似于：

    /home/bjori/tmp/ex.php

### 参见

-   <span class="methodname">Throwable::getFile</span>
