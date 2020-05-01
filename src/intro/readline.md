readline 扩展函数实现了访问 GNU Readline 库的接口.
这些函数提供了可编辑的命令行. 一个例子是在 Bash
中允许你使用箭头按键来插入字符或者翻看历史命令.
因为这个库的交互特性，这个功能在你写的 Web 程序中没多大用处，
但是当你写的脚本被用在<a href="/features/commandline.html" class="link">命令行</a>中时非常有用.

从PHP 7.1.0 开始，这个扩展在Windows上也可用。

**Caution**

readline扩展并非线程安全的！因此，在任何真线程安全的SAPI（例如Apache的mod\_winnt）中使用这个扩展是非常不推荐的！
