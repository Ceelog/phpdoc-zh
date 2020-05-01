在同一个文件中定义多个命名空间
------------------------------

也可以在同一个文件中定义多个命名空间。在同一个文件中定义多个命名空间有两种语法形式。

**示例 \#1 定义多个命名空间，简单组合语法**

``` php
<?php
namespace MyProject;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }

namespace AnotherProject;

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
?>
```

不建议使用这种语法在单个文件中定义多个命名空间。建议使用下面的大括号形式的语法。

**示例 \#2 定义多个命名空间，大括号语法**

``` php
<?php
namespace MyProject {

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
}

namespace AnotherProject {

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
}
?>
```

在实际的编程实践中，非常不提倡在同一个文件中定义多个命名空间。这种方式的主要用于将多个
PHP 脚本合并在同一个文件中。

将全局的非命名空间中的代码与命名空间中的代码组合在一起，只能使用大括号形式的语法。全局代码必须用一个不带名称的
namespace 语句加上大括号括起来，例如：

**示例 \#3 定义多个命名空间和不包含在命名空间中的代码**

``` php
<?php
namespace MyProject {

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
}

namespace { // global code
session_start();
$a = MyProject\connect();
echo MyProject\Connection::start();
}
?>
```

除了开始的declare语句外，命名空间的括号外不得有任何PHP代码。

**示例 \#4 定义多个命名空间和不包含在命名空间中的代码**

``` php
<?php
declare(encoding='UTF-8');
namespace MyProject {

const CONNECT_OK = 1;
class Connection { /* ... */ }
function connect() { /* ... */  }
}

namespace { // 全局代码
session_start();
$a = MyProject\connect();
echo MyProject\Connection::start();
}
?>
```
