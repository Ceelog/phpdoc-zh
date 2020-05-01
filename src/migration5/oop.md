新对象模型
----------

PHP 5 中有个新对象模型（Object Model）。PHP
处理对象的方式完全重写了，允许更佳性能和更多特性。之前版本的
PHP，对象处理方式和原始类型（例如整型和字符串）相同。此方法的缺点是当变量被赋值或作为参数传递给方法时语义上整个对象都被拷贝。在新方法中，对象通过句柄引用，而不是值（可以将句柄当成是对象的标识符）。

很多 PHP 程序员根本没意识到旧的对象模型的这种拷贝怪癖，因此大多数 PHP
应用程序拿来就能运行，或者只做很小的修改。

新对象模型的文档见<a href="/language/oop5.html" class="link">语言参考</a>。

与 PHP 4 的兼容性参见
<a href="/ini/core.html#ini.zend.ze1-compatibility-mode" class="link">zend.ze1_compatibility_mode</a>。
