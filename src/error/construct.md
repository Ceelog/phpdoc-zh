Error::\_\_construct
====================

初始化 error 对象

### 说明

<span class="modifier">public</span> <span
class="methodname">Error::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$message`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$code`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">Throwable</span> `$previous`<span
class="initializer"> = **`NULL`**</span></span> \]\]\] )

初始化 Error。

### 参数

`message`  
错误信息。

`code`  
错误代码。

`previous`  
先前的 throwable，用于异常链。

### 注释

> **Note**:
>
> `message` *不是*二进制安全的。
