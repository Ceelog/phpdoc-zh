执行运算符
----------

PHP 支持一个执行运算符：反引号（\`\`）。注意这不是单引号！PHP
将尝试将反引号中的内容作为 shell
命令来执行，并将其输出信息返回（即，可以赋给一个变量而不是简单地丢弃到标准输出）。使用反引号运算符“\`”的效果与函数
<span class="function">shell\_exec</span> 相同。

``` php
<?php
$output = `ls -al`;
echo "<pre>$output</pre>";
?>
```

> **Note**:
>
> 关闭了 <span class="function">shell\_exec</span>
> 时反引号运算符是无效的。

> **Note**:
>
> 与其它某些语言不同，反引号不能在双引号字符串中使用。

参见手册中<a href="/ref/exec.html" class="link">程序执行函数</a>，<span
class="function">popen</span>，<span class="function">proc\_open</span>
以及
<a href="/features/commandline.html" class="link">PHP 的命令行模式</a>。
