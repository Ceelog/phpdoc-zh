类的自动加载
------------

在编写面向对象（OOP） 程序时，很多开发者为每个类新建一个 PHP 文件。
这会带来一个烦恼：每个脚本的开头，都需要包含（include）一个长长的列表（每个类都有个文件）。

在 PHP 5 中，已经不再需要这样了。 <span
class="function">spl\_autoload\_register</span>
函数可以注册任意数量的自动加载器，当使用尚未被定义的类（class）和接口（interface）时自动去加载。通过注册自动加载器，脚本引擎在
PHP 出错失败前有了最后一个机会加载所需的类。

**小贴士**

尽管 <span class="function">\_\_autoload</span>
函数也能自动加载类和接口，但更建议使用 <span
class="function">spl\_autoload\_register</span> 函数。 <span
class="function">spl\_autoload\_register</span>
提供了一种更加灵活的方式来实现类的自动加载（同一个应用中，可以支持任意数量的加载器，比如第三方库中的）。因此，不再建议使用
<span class="function">\_\_autoload</span>
函数，在以后的版本中它可能被弃用。

> **Note**:
>
> 在 PHP 5.3 之前，\_\_autoload 函数抛出的异常不能被
> <a href="/language/exceptions.html" class="link">catch</a>
> 语句块捕获并会导致一个致命错误（Fatal Error）。 自 PHP 5.3 起，能够
> thrown 自定义的异常（Exception），随后自定义异常类即可使用。
> \_\_autoload 函数可以递归的自动加载自定义异常类。

> **Note**:
>
> 自动加载不可用于 PHP 的 CLI
> <a href="/features/commandline.html" class="link">交互模式</a>。

> **Note**:
>
> 如果类名比如被用于 <span
> class="function">call\_user\_func</span>，则它可能包含一些危险的字符，比如
> *../*。 建议您在这样的函数中不要使用用户的输入，起码需要在 <span
> class="function">\_\_autoload</span> 时验证下输入。

**示例 \#1 自动加载示例**

本例尝试分别从 `MyClass1.php` 和 `MyClass2.php` 文件中加载 *MyClass1* 和
*MyClass2* 类。

``` php
<?php
spl_autoload_register(function ($class_name) {
    require_once $class_name . '.php';
});

$obj  = new MyClass1();
$obj2 = new MyClass2();
?>
```

**示例 \#2 另一个例子**

本例尝试加载接口 *ITest*。

``` php
<?php

spl_autoload_register(function ($name) {
    var_dump($name);
});

class Foo implements ITest {
}

/*
string(5) "ITest"

Fatal error: Interface 'ITest' not found in ...
*/
?>
```

**示例 \#3 自动加载在 PHP 5.3.0+ 中的异常处理**

本例抛出一个异常并在 try/catch 语句块中演示。

``` php
<?php
spl_autoload_register(function ($name) {
    echo "Want to load $name.\n";
    throw new Exception("Unable to load $name.");
});

try {
    $obj = new NonLoadableClass();
} catch (Exception $e) {
    echo $e->getMessage(), "\n";
}
?>
```

以上例程会输出：

    Want to load NonLoadableClass.
    Unable to load NonLoadableClass.

**示例 \#4 自动加载在 PHP 5.3.0+ 中的异常处理 - 没有自定义异常机制**

本例将一个异常抛给不存在的自定义异常处理函数。

``` php
<?php
spl_autoload_register(function ($name) {
    echo "Want to load $name.\n";
    throw new MissingException("Unable to load $name.");
});

try {
    $obj = new NonLoadableClass();
} catch (Exception $e) {
    echo $e->getMessage(), "\n";
}
?>
```

以上例程会输出：

    Want to load NonLoadableClass.
    Want to load MissingException.

    Fatal error: Class 'MissingException' not found in testMissingException.php on line 4

-   <span class="function">unserialize</span>
-   <a href="/var/setup.html#" class="link">unserialize_callback_func</a>
-   <span class="function">spl\_autoload\_register</span>
-   <span class="function">spl\_autoload</span>
-   <span class="function">\_\_autoload</span>
