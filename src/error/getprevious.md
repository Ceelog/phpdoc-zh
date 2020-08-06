Error::getPrevious
==================

返回先前的 Throwable

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

返回先前的 Throwable（ <span
class="methodname">Error::\_\_construct</span> 的第三个参数）。

### 参数

此函数没有参数。

### 返回值

如果有的话，返回先前的 <span
class="classname">Throwable</span>，没有就返回 **`NULL`**。 or
**`NULL`** otherwise.

### 范例

**示例 \#1 <span class="methodname">Error::getPrevious</span> 例子**

循环输出错误栈。

``` php
<?php
class MyCustomError extends Error {}

function doStuff() {
    try {
        throw new InvalidArgumentError("You are doing it wrong!", 112);
    } catch(Error $e) {
        throw new MyCustomError("Something happened", 911, $e);
    }
}


try {
    doStuff();
} catch(Error $e) {
    do {
        printf("%s:%d %s (%d) [%s]\n", $e->getFile(), $e->getLine(), $e->getMessage(), $e->getCode(), get_class($e));
    } while($e = $e->getPrevious());
}
?>
```

以上例程的输出类似于：

    /home/bjori/ex.php:8 Something happened (911) [MyCustomError]
    /home/bjori/ex.php:6 You are doing it wrong! (112) [InvalidArgumentError]

### 参见

-   <span class="methodname">Throwable::getPrevious</span>
