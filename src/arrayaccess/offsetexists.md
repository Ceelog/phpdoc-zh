ArrayAccess::offsetExists
=========================

检查一个偏移位置是否存在

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">boolean</span> <span
class="methodname">ArrayAccess::offsetExists</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> )

检查一个偏移位置是否存在。

对一个实现了 <span class="classname">ArrayAccess</span> 接口的对象使用
<span class="function">isset</span> 或 <span
class="function">empty</span> 时，此方法将执行。

> **Note**:
>
> 当使用 <span class="function">empty</span> 并且仅当 <span
> class="function">ArrayAccess::offsetExists</span> 返回 **`TRUE`**
> 时，<span class="function">ArrayAccess::offsetGet</span>
> 将被调用以检查是为否空。

### 参数

`offset`  
需要检查的偏移位置。

### 返回值

成功时返回 **`TRUE`**， 或者在失败时返回 **`FALSE`**。

> **Note**:
>
> 如果一个非布尔型返回值被返回，将被转换为<span
> class="type">布尔型</span>。

### 范例

**示例 \#1 <span class="function">ArrayAccess::offsetExists</span>
范例**

``` php
<?php
class obj implements arrayaccess {
    public function offsetSet($offset, $value) {
        var_dump(__METHOD__);
    }
    public function offsetExists($var) {
        var_dump(__METHOD__);
        if ($var == "foobar") {
            return true;
        }
        return false;
    }
    public function offsetUnset($var) {
        var_dump(__METHOD__);
    }
    public function offsetGet($var) {
        var_dump(__METHOD__);
        return "value";
    }
}

$obj = new obj;

echo "Runs obj::offsetExists()\n";
var_dump(isset($obj["foobar"]));

echo "\nRuns obj::offsetExists() and obj::offsetGet()\n";
var_dump(empty($obj["foobar"]));

echo "\nRuns obj::offsetExists(), *not* obj:offsetGet() as there is nothing to get\n";
var_dump(empty($obj["foobaz"]));
?>
```

以上例程的输出类似于：

    Runs obj::offsetExists()
    string(17) "obj::offsetExists"
    bool(true)

    Runs obj::offsetExists() and obj::offsetGet()
    string(17) "obj::offsetExists"
    string(14) "obj::offsetGet"
    bool(false)

    Runs obj::offsetExists(), *not* obj:offsetGet() as there is nothing to get
    string(17) "obj::offsetExists"
    bool(true)
