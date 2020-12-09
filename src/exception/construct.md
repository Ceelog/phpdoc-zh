Exception::\_\_construct
========================

异常构造函数

### 说明

<span class="modifier">public</span> <span
class="methodname">Exception::\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$message`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$code`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">Throwable</span> `$previous`<span
class="initializer"> = **`null`**</span></span> \]\]\] )

异常构造函数。

### 参数

`message`  
抛出的异常消息内容。

`code`  
异常代码。

`previous`  
异常链中的前一个异常。

> **Note**: <span class="simpara"> 如果子类的 $code 和 $message
> 属性已设置，在调用 Exception 父类的构造器时可以省略默认参数。 </span>

### 更新日志

| 版本  | 说明                                                               |
|-------|--------------------------------------------------------------------|
| 7.0.0 | `previous` 参数现在是 <span class="type">Throwable</span> 类型了。 |
| 5.3.0 | 增加`previous`参数。                                               |

### 注释

> **Note**:
>
> The `message` is *NOT* binary safe.
