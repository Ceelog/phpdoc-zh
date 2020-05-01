这些函数中使用的模式语法非常类似
perl。表达式必须用分隔符闭合，比如一个正斜杠(/)。
分隔符可以使任意非字母数字，除反斜杠(\\)和空字节之外的非空白 ascii
字符。 如果分隔符 在表达式中使用，需要使用反斜线进行转义。自php
4.0.4开始，可以使用 perl 样式的()、 {}、 \[\] 以及 \<\> 作为分隔符。
更详细的解释参见<a href="/pcre/pattern.html#PCRE%20正则语法" class="link">模式语法</a>。

结束分隔符后面可以紧跟模式修饰符来影响匹配效果。
参见<a href="/pcre/pattern.html#正则表达式模式中可用的模式修饰符" class="link">模式修饰符</a>。

PHP也支持使用
<a href="/book/regex.html" class="link">POSIX 扩展正则表达式函数</a> 的
POSIX 扩展语法的正则表达式。

> **Note**:
>
> 这个扩展维护了一个已编译正则表达式的全局线程化缓存(最大4096)。

**Warning**

你应该知道一些 PCRE
的限制。阅读<a href="http://www.pcre.org/pcre.txt" class="link external">» http://www.pcre.org/pcre.txt</a>
获取更详细信息。

PCRE 库是一个实现了与 perl 5
在语法和语义上略有差异(详见下文)的正则表达式模式匹配功能的函数集。
当前的实现对应于 perl 5.005。
