扩展（extend） PHP 内置的异常处理类
-----------------------------------

用户可以用自定义的异常处理类来扩展 PHP
内置的异常处理类。以下的代码说明了在内置的异常处理类中，哪些属性和方法在子类中是可访问和可继承的。译者注：以下这段代码只为说明内置异常处理类的结构，它并不是一段有实际意义的可用代码。

**示例 \#1 内置的异常处理类**

``` php
<?php
class Exception
{
    protected $message = 'Unknown exception';   // 异常信息
    private   $string;                          // __toString cache
    protected $code = 0;                        // 用户自定义异常代码
    protected $file;                            // 发生异常的文件名
    protected $line;                            // 发生异常的代码行号
    private   $trace;                           // backtrace
    private   $previous;                        // previous exception if nested exception

    public function __construct($message = null, $code = 0, Exception $previous = null);

    final private function __clone();           // Inhibits cloning of exceptions.

    final public  function getMessage();        // 返回异常信息
    final public  function getCode();           // 返回异常代码
    final public  function getFile();           // 返回发生异常的文件名
    final public  function getLine();           // 返回发生异常的代码行号
    final public  function getTrace();          // backtrace() 数组
    final public  function getPrevious();       // 之前的 exception
    final public  function getTraceAsString();  // 已格成化成字符串的 getTrace() 信息

    // Overrideable
    public function __toString();               // 可输出的字符串
}
?>
```

如果使用自定义的类来扩展内置异常处理类，并且要重新定义<a href="/language/oop5/decon.html" class="link">构造函数</a>的话，建议同时调用
<a href="/language/oop5/paamayim-nekudotayim.html" class="link">parent::__construct()</a>
来检查所有的变量是否已被赋值。当对象要输出字符串的时候，可以重载
<a href="/language/oop5/magic.html" class="link">__toString()</a>
并自定义输出的样式。

> **Note**:
>
> Exception 对象不能被复制。尝试对 Exception
> <a href="/language/oop5/cloning.html" class="link">对象复制</a>
> 会导致一个 **`E_ERROR`** 级别的错误。

**示例 \#2 扩展 PHP 内置的异常处理类 (PHP 5.3.0+)**

``` php
<?php
/**
 * 自定义一个异常处理类
 */
class MyException extends Exception
{
    // 重定义构造器使 message 变为必须被指定的属性
    public function __construct($message, $code = 0, Exception $previous = null) {
        // 自定义的代码

        // 确保所有变量都被正确赋值
        parent::__construct($message, $code, $previous);
    }

    // 自定义字符串输出的样式
    public function __toString() {
        return __CLASS__ . ": [{$this->code}]: {$this->message}\n";
    }

    public function customFunction() {
        echo "A custom function for this type of exception\n";
    }
}


/**
 * 创建一个用于测试异常处理机制的类
 */
class TestException
{
    public $var;

    const THROW_NONE    = 0;
    const THROW_CUSTOM  = 1;
    const THROW_DEFAULT = 2;

    function __construct($avalue = self::THROW_NONE) {

        switch ($avalue) {
            case self::THROW_CUSTOM:
                // 抛出自定义异常
                throw new MyException('1 is an invalid parameter', 5);
                break;

            case self::THROW_DEFAULT:
                // 抛出默认的异常
                throw new Exception('2 is not allowed as a parameter', 6);
                break;

            default: 
                // 没有异常的情况下，创建一个对象
                $this->var = $avalue;
                break;
        }
    }
}


// 例子 1
try {
    $o = new TestException(TestException::THROW_CUSTOM);
} catch (MyException $e) {      // 捕获异常
    echo "Caught my exception\n", $e;
    $e->customFunction();
} catch (Exception $e) {        // 被忽略
    echo "Caught Default Exception\n", $e;
}

// Continue execution
var_dump($o); // Null
echo "\n\n";


// 例子 2
try {
    $o = new TestException(TestException::THROW_DEFAULT);
} catch (MyException $e) {      //  不能匹配异常的种类，被忽略

    echo "Caught my exception\n", $e;
    $e->customFunction();
} catch (Exception $e) {        // 捕获异常
    echo "Caught Default Exception\n", $e;
}

// 执行后续代码
var_dump($o); // Null
echo "\n\n";


// 例子 3
try {
    $o = new TestException(TestException::THROW_CUSTOM);
} catch (Exception $e) {        // 捕获异常
    echo "Default Exception caught\n", $e;
}

// 执行后续代码
var_dump($o); // Null
echo "\n\n";


// 例子 4
try {
    $o = new TestException();
} catch (Exception $e) {        // 没有异常，被忽略
    echo "Default Exception caught\n", $e;
}

// 执行后续代码
var_dump($o); // TestException
echo "\n\n";
?>
```

> **Note**:
>
> Versions of PHP 5, prior to PHP 5.3.0 do not support nesting of
> exceptions. The following code fragment can be used as a replacement
> MyException class if you wish to run this example.
>
> ``` php
> <?php
> /**
>  * Define a custom exception class
>  */
> class MyException extends Exception
> {
>     // Redefine the exception so message isn't optional
>     public function __construct($message, $code = 0) {
>         // some code
>     
>         // make sure everything is assigned properly
>         parent::__construct($message, $code);
>     }
>
>     // custom string representation of object
>     public function __toString() {
>         return __CLASS__ . ": [{$this->code}]: {$this->message}\n";
>     }
>
>     public function customFunction() {
>         echo "A custom function for this type of exception\n";
>     }
> }
> ?>
> ```
