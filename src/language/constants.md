常量
====

**目录**

-   [语法](/language/constants/syntax.html)
-   [魔术常量](/language/constants/predefined.html)

常量是一个简单值的标识符（名字）。如同其名称所暗示的，在脚本执行期间该值不能改变（除了所谓的<a href="/language/constants/predefined.html" class="link">魔术常量</a>，它们其实不是常量）。常量默认为大小写敏感。传统上常量标识符总是大写的。

常量名和其它任何 PHP
标签遵循同样的命名规则。合法的常量名以字母或下划线开始，后面跟着任何字母，数字或下划线。用正则表达式是这样表达的：*\[a-zA-Z\_\\x7f-\\xff\]\[a-zA-Z0-9\_\\x7f-\\xff\]\**。

**小贴士**

请参见<a href="/userlandnaming.html" class="xref">用户空间命名指南</a>。

**示例 \#1 合法与非法的常量名**

``` php
<?php

// 合法的常量名
define("FOO",     "something");
define("FOO2",    "something else");
define("FOO_BAR", "something more");

// 非法的常量名
define("2FOO",    "something");

// 下面的定义是合法的，但应该避免这样做：(自定义常量不要以__开头)
// 也许将来有一天PHP会定义一个__FOO__的魔术常量
// 这样就会与你的代码相冲突
define("__FOO__", "something");

?>
```

> **Note**: <span class="simpara"> 在这里，字母指的是 a-z，A-Z，以及从
> 127 到 255（0x7f-0xff）的 ASCII 字符。 </span>

和
<a href="/language/variables/predefined.html" class="link">superglobals</a>
一样，常量的范围是全局的。不用管作用区域就可以在脚本的任何地方访问常量。有关作用区域的更多信息请阅读手册中的<a href="/language/variables/scope.html" class="link">变量范围</a>。
