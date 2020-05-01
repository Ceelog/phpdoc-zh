counter\_create
===============

创建一个包含单个数值的计数器。

### 说明

<span class="type">resource</span> <span
class="methodname">counter\_create</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">integer</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">integer</span> `$flags`</span> \]\] )

创建一个包含单个数值的计数器。

### 参数

name  
<span class="simpara"> 新的计数器名称。 </span>

initial\_value  
<span class="simpara"> 计数器的初值值. 默认为零(0)。 </span>

flags  
<span class="simpara"> 新计数器的标志, 从形如 *COUNTER\_FLAG\_\**
的常量中选择。 </span>

### 返回值

返回计数器资源。
