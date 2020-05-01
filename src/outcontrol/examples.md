范例
====

**目录**

-   [基本用法](/outcontrol/examples.html#基本用法)

基本用法
--------

**示例 \#1 输出控制举例**

``` php
<?php

ob_start();
echo "Hello\n";

setcookie("cookiename", "cookiedata");

ob_end_flush();

?>
```

在上面的例子中，<span
class="function">echo</span>函数的输出将一直被保存在输出缓冲区中直到调用
<span class="function">ob\_end\_flush</span> 。同时，对<span
class="function">setcookie</span>的调用也成功存储了一个cookie,而不会引起错误。（正常情况下，在数据被发送到浏览器后，就不能再发送http头信息了。）
