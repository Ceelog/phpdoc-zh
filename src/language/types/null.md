NULL
----

特殊的 **`null`** 值表示一个变量没有值。<span class="type">NULL</span>
类型唯一可能的值就是 **`null`**。

在下列情况下一个变量被认为是 **`null`**：

-   被赋值为 **`null`**。

-   尚未被赋值。

-   被 <span class="function">unset</span>。

### 语法

**`null`** 类型只有一个值，就是不区分大小写的常量 **`null`**。

``` php
<?php
$var = NULL;       
?>
```

参见 <span class="function">is\_null</span> 和 <span
class="function">unset</span>。

### 转换到 *NULL*

**Warning**

本特性已自 PHP 7.2.0 起*废弃*。强烈建议不要使用本特性。

使用 *(unset) $var* 将一个变量转换为 <span class="type">null</span>
将*不会*删除该变量或 unset 其值。仅是返回 **`null`** 值而已。
