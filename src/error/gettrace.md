Error::getTrace
===============

获取调用栈（stack trace）

### 说明

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

返回 stack trace。

### 参数

此函数没有参数。

### 返回值

返回 <span class="type">array</span> 的 stack trace。

### 范例

**示例 \#1 <span class="function">Error::getTrace</span> 例子**

``` php
<?php
function test() {
 throw new Error;
}

try {
 test();
} catch(Error $e) {
 var_dump($e->getTrace());
}
?>
```

以上例程的输出类似于：

    array(1) {
      [0]=>
      array(4) {
        ["file"]=>
        string(22) "/home/bjori/tmp/ex.php"
        ["line"]=>
        int(7)
        ["function"]=>
        string(4) "test"
        ["args"]=>
        array(0) {
        }
      }
    }

### 参见

-   <span class="methodname">Throwable::getTrace</span>
