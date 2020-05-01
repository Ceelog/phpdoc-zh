范例
====

**示例 \#1 正则表达式例子**

``` php
<?php
// $string 中任意位置找到 "abc" 就返回 true。
ereg("abc", $string);            

// $string 中起始位置找到 "abc" 就返回 true。
ereg("^abc", $string);

// $string 末尾找到 "abc" 就返回 true。
ereg("abc$", $string);

// 客户浏览器是 Netscape 2、 3 或 MSIE 3 就返回 true。
eregi("(ozilla.[23]|MSIE.3)", $_SERVER["HTTP_USER_AGENT"]);

// 三个空格分割单词为 $regs[1]、 $regs[2]、 $regs[3]。
ereg("([[:alnum:]]+) ([[:alnum:]]+) ([[:alnum:]]+)", $string, $regs); 

// $string 头部加一个 <br /> 标签。
$string = ereg_replace("^", "<br />", $string); 

// $string 尾部添加一个 <br /> 标签。
$string = ereg_replace("$", "<br />", $string); 

// 删除 $string 里的换行符。
$string = ereg_replace("\n", "", $string);
?>
```
