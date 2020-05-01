namespace关键字和\_\_NAMESPACE\_\_常量
--------------------------------------

PHP支持两种抽象的访问当前命名空间内部元素的方法，**`__NAMESPACE__`**
魔术常量和*namespace*关键字。

常量**`__NAMESPACE__`**的值是包含当前命名空间名称的字符串。在全局的，不包括在任何命名空间中的代码，它包含一个空的字符串。

**示例 \#1 \_\_NAMESPACE\_\_ 示例, 在命名空间中的代码**

``` php
<?php
namespace MyProject;

echo '"', __NAMESPACE__, '"'; // 输出 "MyProject"
?>
```

**示例 \#2 \_\_NAMESPACE\_\_ 示例，全局代码**

``` php
<?php

echo '"', __NAMESPACE__, '"'; // 输出 ""
?>
```

常量 **`__NAMESPACE__`** 在动态创建名称时很有用，例如：

**示例 \#3 使用\_\_NAMESPACE\_\_动态创建名称**

``` php
<?php
namespace MyProject;

function get($classname)
{
    $a = __NAMESPACE__ . '\\' . $classname;
    return new $a;
}
?>
```

关键字 *namespace*
可用来显式访问当前命名空间或子命名空间中的元素。它等价于类中的 *self*
操作符。

**示例 \#4 namespace操作符，命名空间中的代码**

``` php
<?php
namespace MyProject;

use blah\blah as mine; // see "Using namespaces: importing/aliasing"

blah\mine(); // calls function MyProject\blah\mine()
namespace\blah\mine(); // calls function MyProject\blah\mine()

namespace\func(); // calls function MyProject\func()
namespace\sub\func(); // calls function MyProject\sub\func()
namespace\cname::method(); // calls static method "method" of class MyProject\cname
$a = new namespace\sub\cname(); // instantiates object of class MyProject\sub\cname
$b = namespace\CONSTANT; // assigns value of constant MyProject\CONSTANT to $b
?>
```

**示例 \#5 namespace操作符, 全局代码**

``` php
<?php

namespace\func(); // calls function func()
namespace\sub\func(); // calls function sub\func()
namespace\cname::method(); // calls static method "method" of class cname
$a = new namespace\sub\cname(); // instantiates object of class sub\cname
$b = namespace\CONSTANT; // assigns value of constant CONSTANT to $b
?>
```
