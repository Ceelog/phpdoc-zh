ErrorException::\_\_construct
=============================

构造一个异常（Exception）

### 说明

<span class="modifier">public</span> <span
class="methodname">ErrorException::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$message`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$code`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$severity`<span
class="initializer"> = E\_ERROR</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$filename`<span
class="initializer"> = \_\_FILE\_\_</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$lineno`<span
class="initializer"> = \_\_LINE\_\_</span></span> \[, <span
class="methodparam"><span class="type">Exception</span> `$previous`<span
class="initializer"> = **`NULL`**</span></span> \]\]\]\]\]\] )

构造一个异常（Exception）。

### 参数

`message`  
抛出的异常消息内容。

`code`  
异常代码。

`severity`  
异常的严重级别。

> **Note**:
>
> severity 可以是任意 <span class="type">integer</span>
> 值，即<a href="/errorfunc/constants.html" class="link">错误常量</a>里面的值。

`filename`  
抛出异常所在的文件名。

`lineno`  
抛出异常所在的行号。

`previous`  
异常链中的前一个异常。

### 更新日志

| 版本  | 说明                   |
|-------|------------------------|
| 5.3.0 | 增加 `previous` 参数。 |
