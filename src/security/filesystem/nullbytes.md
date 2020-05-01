Null 字符问题
-------------

由于 PHP 的文件系统操作是基于 C
语言的函数的，所以它可能会以您意想不到的方式处理 Null 字符。 Null字符在
C 语言中用于标识字符串结束，一个完整的字符串是从其开头到遇见 Null
字符为止。 以下代码演示了类似的攻击：

**示例 \#1 会被 Null 字符问题攻击的代码**

``` php
<?php
$file = $_GET['file']; // "../../etc/passwd\0"
if (file_exists('/home/wwwrun/'.$file.'.php')) {
    // file_exists will return true as the file /home/wwwrun/../../etc/passwd exists
    include '/home/wwwrun/'.$file.'.php';
    // the file /etc/passwd will be included
}
?>
```

因此，任何用于操作文件系统的字符串（译注：特别是程序外部输入的字符串）都必须经过适当的检查。以下是上述例子的改进版本：

**示例 \#2 验证输入的正确做法**

``` php
<?php
$file = $_GET['file']; 

// 对字符串进行白名单检查
switch ($file) {
    case 'main':
    case 'foo':
    case 'bar':
        include '/home/wwwrun/include/'.$file.'.php';
        break;
    default:
        include '/home/wwwrun/include/main.php';
}
?>
```
