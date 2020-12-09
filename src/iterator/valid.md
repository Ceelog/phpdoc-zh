Iterator::valid
===============

检查当前位置是否有效

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">bool</span> <span
class="methodname">Iterator::valid</span> ( <span
class="methodparam">void</span> )

此方法在 <span class="methodname">Iterator::rewind</span> 和 <span
class="methodname">Iterator::next</span>
方法之后被调用以此用来检查当前位置是否有效。

### 参数

此函数没有参数。

### 返回值

返回将被转换为<span class="type">布尔型</span>。成功时返回 **`true`**，
或者在失败时返回 **`false`**。
