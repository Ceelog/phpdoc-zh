Exception::getPrevious
======================

返回异常链中的前一个异常

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

返回异常链中的前一个异常（ <span
class="methodname">Exception::\_\_construct</span>方法的第三个参数）。

### 参数

此函数没有参数。

### 返回值

返回异常链中的前一个异常 <span
class="classname">Throwable</span>，否则返回**`null`**。

### 更新日志

| 版本  | 说明                                                            |
|-------|-----------------------------------------------------------------|
| 7.0.0 | 返回类型的定义改成了 <span class="classname">Throwable</span>。 |

### 范例

**示例 \#1 <span class="methodname">Exception::getPrevious</span>示例**

追踪异常，并循环打印。

``` php
<?php
class MyCustomException extends Exception {}

function doStuff() {
    try {
        throw new InvalidArgumentException("You are doing it wrong!", 112);
    } catch(Exception $e) {
        throw new MyCustomException("Something happend", 911, $e);
    }
}


try {
    doStuff();
} catch(Exception $e) {
    do {
        printf("%s:%d %s (%d) [%s]\n", $e->getFile(), $e->getLine(), $e->getMessage(), $e->getCode(), get_class($e));
    } while($e = $e->getPrevious());
}
?>
```

以上例程的输出类似于：

    /home/bjori/ex.php:8 Something happend (911) [MyCustomException]
    /home/bjori/ex.php:6 You are doing it wrong! (112) [InvalidArgumentException]

### 参见

-   <span class="methodname">Throwable::getPrevious</span>
