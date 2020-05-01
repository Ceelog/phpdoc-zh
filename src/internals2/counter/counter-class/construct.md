Counter::\_\_construct
======================

创建一个包含单一数值的计数器实例。

### 说明

<span class="methodname">Counter::\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">integer</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">integer</span> `$flags`</span> \]\] )

创建一个包含单一数值的 Counter 实例。

### 参数

name  
<span class="simpara"> 新计数器的名称。 </span>

initial\_value  
<span class="simpara"> 计数器的初始值。默认为零(0)。 </span>

flags  
<span class="simpara"> 新计数器的标志，可在形如 *COUNTER\_FLAG\_\**
的常量中选择。 </span>

### 返回值

成功则返回 Counter 对象。

### 错误／异常

<span class="function">Counter::\_\_construct</span>
在有错时抛出一个异常(Exception)。
