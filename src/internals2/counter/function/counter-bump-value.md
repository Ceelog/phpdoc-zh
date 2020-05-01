counter\_bump\_value
====================

更新计数器资源的当前值。

### 说明

<span class="type">void</span> <span
class="methodname">counter\_bump\_value</span> ( <span
class="methodparam"><span class="type">resource</span> `$counter`</span>
, <span class="methodparam"><span class="type">integer</span>
`$offset`</span> )

<span class="function">counter\_bump\_value</span>
更新计数器资源的当前值。

### 参数

`counter`  
<span class="simpara"> 要操作的计数器资源。 </span>

`offset`  
<span class="simpara"> 计数器值的变化量。可为负数。 </span>

### 参见

-   <span class="function">counter\_get\_value</span>
-   <span class="function">counter\_reset\_value</span>
