PHP 标记
--------

当解析一个文件时，PHP 会寻找起始和结束标记，也就是 *\<?php* 和
*?\>*，这告诉 PHP 开始和停止解析二者之间的代码。此种解析方式使得 PHP
可以被嵌入到各种不同的文档中去，而任何起始和结束标记之外的部分都会被 PHP
解析器忽略。

PHP 也允许使用短标记 *\<?* 和 *?\>*，但不鼓励使用。只有通过激活
`php.ini` 中的
<a href="/ini/core.html#ini.short-open-tag" class="link">short_open_tag</a>
配置指令或者在编译 PHP 时使用了配置选项 **--enable-short-tags**
时才能使用短标记。

如果文件内容是纯 PHP 代码，最好在文件末尾删除 PHP 结束标记。这可以避免在
PHP 结束标记之后万一意外加入了空格或者换行符，会导致 PHP
开始输出这些空白，而脚本中此时并无输出的意图。

``` php
<?php
echo "Hello world";

// ... more code

echo "Last statement";

// 脚本至此结束，并无 PHP 结束标记
```
