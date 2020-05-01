NULL
----

特殊的 **`NULL`** 值表示一个变量没有值。<span class="type">NULL</span>
类型唯一可能的值就是 **`NULL`**。

在下列情况下一个变量被认为是 **`NULL`**：

-   被赋值为 **`NULL`**。

-   尚未被赋值。

-   被 <span class="function">unset</span>。

### 语法

**`NULL`** 类型只有一个值，就是不区分大小写的常量 **`NULL`**。

``` php
<?php
$var = NULL;       
?>
```

参见 <span class="function">is\_null</span> 和 <span
class="function">unset</span>。

### 转换到 *NULL*

使用 *(unset) $var* 将一个变量转换为 <span class="type">null</span>
将*不会*删除该变量或 unset 其值。仅是返回 **`NULL`** 值而已。
