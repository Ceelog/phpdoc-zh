命名空间概述
------------

什么是命名空间？从广义上来说，命名空间是一种封装事物的方法。在很多地方都可以见到这种抽象概念。例如，在操作系统中目录用来将相关文件分组，对于目录中的文件来说，它就扮演了命名空间的角色。具体举个例子，文件
*foo.txt* 可以同时在目录*/home/greg* 和 */home/other*
中存在，但在同一个目录中不能存在两个 *foo.txt* 文件。另外，在目录
*/home/greg* 外访问 *foo.txt*
文件时，我们必须将目录名以及目录分隔符放在文件名之前得到
*/home/greg/foo.txt*。这个原理应用到程序设计领域就是命名空间的概念。

在PHP中，命名空间用来解决在编写类库或应用程序时创建可重用的代码如类或函数时碰到的两类问题：

1.  <span class="simpara">
    用户编写的代码与PHP内部的类/函数/常量或第三方类/函数/常量之间的名字冲突。
    </span>
2.  <span class="simpara">
    为很长的标识符名称(通常是为了缓解第一类问题而定义的)创建一个别名（或简短）的名称，提高源代码的可读性。
    </span>

PHP
命名空间提供了一种将相关的类、函数和常量组合到一起的途径。下面是一个说明
PHP 命名空间语法的示例：

**示例 \#1 命名空间语法示例**

``` php
<?php
namespace my\name; // 参考 "定义命名空间" 小节

class MyClass {}
function myfunction() {}
const MYCONST = 1;

$a = new MyClass;
$c = new \my\name\MyClass; // 参考 "全局空间" 小节

$a = strlen('hi'); // 参考 "使用命名空间：后备全局函数/常量" 小节

$d = namespace\MYCONST; // 参考 "namespace操作符和__NAMESPACE__常量” 小节

$d = __NAMESPACE__ . '\MYCONST';
echo constant($d); // 参考 "命名空间和动态语言特征" 小节
?>
```

> **Note**:
>
> 名为*PHP*或*php*的命名空间，以及以这些名字开头的命名空间（例如*PHP\\Classes*）被保留用作语言内核使用，而不应该在用户空间的代码中使用。
