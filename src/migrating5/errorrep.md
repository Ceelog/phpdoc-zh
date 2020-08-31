错误报告
--------

自 PHP 5 起引进了新常量 **`E_STRICT`**，其值为
*2048*。它提供了对用户代码的协同性和向前兼容性的运行时 PHP
建议，有助于使用户保持最新和最好的编程风格。例如在使用已过时的函数时
STRICT 信息会提出警告。

> **Note**: <span class="simpara"> **`E_ALL`** 不包括
> **`E_STRICT`**，因此其默认未激活。你必需明确设置错误级别包括
> **`E_STRICT`** 来查看这些信息。 </span>

更多信息请参阅
<a href="/errorfunc/constants.html" class="link">预定义常量</a>。
