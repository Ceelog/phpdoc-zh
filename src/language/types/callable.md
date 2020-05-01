Callback / Callable 类型
------------------------

自 PHP 5.4 起可用 <span class="type">callable</span> 类型指定回调类型
callback。本文档基于同样理由使用 <span class="type">callback</span>
类型信息。

一些函数如 <span class="function">call\_user\_func</span> 或 <span
class="function">usort</span>
可以接受用户自定义的回调函数作为参数。回调函数不止可以是简单函数，还可以是对象的方法，包括静态类方法。

### 传递

PHP是将函数以<span class="type">string</span>形式传递的。
可以使用任何内置或用户自定义函数，但除了语言结构例如：<span
class="function">array</span>，<span class="function">echo</span>，<span
class="function">empty</span>，<span class="function">eval</span>，<span
class="function">exit</span>，<span class="function">isset</span>，<span
class="function">list</span>，<span class="function">print</span> 或
<span class="function">unset</span>。

一个已实例化的 <span class="type">object</span> 的方法被作为 <span
class="type">array</span> 传递，下标 0 包含该 <span
class="type">object</span>，下标 1 包含方法名。 在同一个类里可以访问
protected 和 private 方法。

静态类方法也可不经实例化该类的对象而传递，只要在下标 0
中包含类名而不是对象。自 PHP 5.2.3 起，也可以传递
*'ClassName::methodName'*。

除了普通的用户自定义函数外，也可传递
<a href="/functions/anonymous.html" class="link">匿名函数</a>
给回调参数。

**示例 \#1 回调函数示例**

``` php
<?php 

// An example callback function
function my_callback_function() {
    echo 'hello world!';
}

// An example callback method
class MyClass {
    static function myCallbackMethod() {
        echo 'Hello World!';
    }
}

// Type 1: Simple callback
call_user_func('my_callback_function'); 

// Type 2: Static class method call
call_user_func(array('MyClass', 'myCallbackMethod')); 

// Type 3: Object method call
$obj = new MyClass();
call_user_func(array($obj, 'myCallbackMethod'));

// Type 4: Static class method call (As of PHP 5.2.3)
call_user_func('MyClass::myCallbackMethod');

// Type 5: Relative static class method call (As of PHP 5.3.0)
class A {
    public static function who() {
        echo "A\n";
    }
}

class B extends A {
    public static function who() {
        echo "B\n";
    }
}

call_user_func(array('B', 'parent::who')); // A

// Type 6: Objects implementing __invoke can be used as callables (since PHP 5.3)
class C {
    public function __invoke($name) {
        echo 'Hello ', $name, "\n";
    }
}

$c = new C();
call_user_func($c, 'PHP!');
?>
```

**示例 \#2 使用 Closure 的示例**

``` php
<?php
// Our closure
$double = function($a) {
    return $a * 2;
};

// This is our range of numbers
$numbers = range(1, 5);

// Use the closure as a callback here to 
// double the size of each element in our 
// range
$new_numbers = array_map($double, $numbers);

print implode(' ', $new_numbers);
?>
```

以上例程会输出：

    2 4 6 8 10

> **Note**:
>
> 在函数中注册有多个回调内容时(如使用 <span
> class="function">call\_user\_func</span> 与 <span
> class="function">call\_user\_func\_array</span>)，如在前一个回调中有未捕获的异常，其后的将不再被调用。
