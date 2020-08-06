Error::getFile
==============

获取错误发生时的文件

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

获取错误发生时的文件名称。

### 参数

此函数没有参数。

### 返回值

返回错误发生时的文件名。

### 范例

**示例 \#1 <span class="function">Error::getFile</span> 例子**

``` php
<?php
try {
    throw new Error;
} catch(Error $e) {
    echo $e->getFile();
}
?>
```

以上例程的输出类似于：

    /home/bjori/tmp/ex.php

### 参见

-   <span class="methodname">Throwable::getFile</span>
