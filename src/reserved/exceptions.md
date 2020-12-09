预定义异常
==========

**目录**

-   [Exception](/class/exception.html) — Exception
    -   [Exception::\_\_construct](/exception/construct.html) —
        异常构造函数
    -   [Exception::getMessage](/exception/getmessage.html) —
        获取异常消息内容
    -   [Exception::getPrevious](/exception/getprevious.html) —
        返回异常链中的前一个异常
    -   [Exception::getCode](/exception/getcode.html) — 获取异常代码
    -   [Exception::getFile](/exception/getfile.html) —
        创建异常时的程序文件名称
    -   [Exception::getLine](/exception/getline.html) —
        获取创建的异常所在文件中的行号
    -   [Exception::getTrace](/exception/gettrace.html) —
        获取异常追踪信息
    -   [Exception::getTraceAsString](/exception/gettraceasstring.html)
        — 获取字符串类型的异常追踪信息
    -   [Exception::\_\_toString](/exception/tostring.html) —
        将异常对象转换为字符串
    -   [Exception::\_\_clone](/exception/clone.html) — 异常克隆
-   [ErrorException](/class/errorexception.html) — ErrorException
    -   [ErrorException::\_\_construct](/errorexception/construct.html)
        — 构造一个异常（Exception）
    -   [ErrorException::getSeverity](/errorexception/getseverity.html)
        — 获取异常的严重程度
-   [Error](/class/error.html) — Error
    -   [Error::\_\_construct](/error/construct.html) — 初始化 error
        对象
    -   [Error::getMessage](/error/getmessage.html) — 获取错误信息
    -   [Error::getPrevious](/error/getprevious.html) — 返回先前的
        Throwable
    -   [Error::getCode](/error/getcode.html) — 获取错误代码
    -   [Error::getFile](/error/getfile.html) — 获取错误发生时的文件
    -   [Error::getLine](/error/getline.html) — 获取错误发生时的行号
    -   [Error::getTrace](/error/gettrace.html) — 获取调用栈（stack
        trace）
    -   [Error::getTraceAsString](/error/gettraceasstring.html) —
        获取字符串形式的调用栈（stack trace）
    -   [Error::\_\_toString](/error/tostring.html) — error 的字符串表达
    -   [Error::\_\_clone](/error/clone.html) — 克隆 error
-   [ArgumentCountError](/class/argumentcounterror.html) —
    ArgumentCountError
-   [ArithmeticError](/class/arithmeticerror.html) — ArithmeticError
-   [AssertionError](/class/assertionerror.html) — AssertionError
-   [DivisionByZeroError](/class/divisionbyzeroerror.html) —
    DivisionByZeroError
-   [CompileError](/class/compileerror.html) — CompileError
-   [ParseError](/class/parseerror.html) — ParseError
-   [TypeError](/class/typeerror.html) — TypeError

参见 <a href="/spl/exceptions.html" class="link">SPL 异常处理</a>

简介
----

<span class="ooclass">**Exception**</span>是所有异常的基类。

类摘要
------

**Exception**

<span class="ooclass"> class **Exception** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$message`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$code`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">Throwable</span> `$previous`<span
class="initializer"> = **`null`**</span></span> \]\]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getCode</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span class="methodname">getFile</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getLine</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span class="methodname">getTrace</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">\_\_clone</span> ( <span
class="methodparam">void</span> )

}

属性
----

`message`  
异常消息内容

`code`  
异常代码

`file`  
抛出异常的文件名

`line`  
抛出异常在该文件中的行号

简介
----

错误异常。

类摘要
------

**ErrorException**

<span class="ooclass"> class **ErrorException** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Exception**
</span> {

/\* 属性 \*/

<span class="modifier">protected</span> <span class="type">int</span>
`$severity` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$message`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$code`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$severity`<span
class="initializer"> = E\_ERROR</span></span> \[, <span
class="methodparam"><span class="type">string</span> `$filename`<span
class="initializer"> = \_\_FILE\_\_</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$lineno`<span
class="initializer"> = \_\_LINE\_\_</span></span> \[, <span
class="methodparam"><span class="type">Exception</span> `$previous`<span
class="initializer"> = **`null`**</span></span> \]\]\]\]\]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">getSeverity</span> ( <span
class="methodparam">void</span> )

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Exception::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Exception::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Exception::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Exception::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Exception::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Exception::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

属性
----

`severity`  
异常级别

范例
----

**示例 \#1 使用<span
class="function">set\_error\_handler</span>函数将错误信息托管至ErrorException**

``` php
<?php
function exception_error_handler($errno, $errstr, $errfile, $errline ) {
    throw new ErrorException($errstr, 0, $errno, $errfile, $errline);
}
set_error_handler("exception_error_handler");

/* Trigger exception */
strpos();
?>
```

以上例程的输出类似于：

    Fatal error: Uncaught exception 'ErrorException' with message 'Wrong parameter count for strpos()' in /home/bjori/tmp/ex.php:8
    Stack trace:
    #0 [internal function]: exception_error_handler(2, 'Wrong parameter...', '/home/bjori/php...', 8, Array)
    #1 /home/bjori/php/cleandocs/test.php(8): strpos()
    #2 {main}
      thrown in /home/bjori/tmp/ex.php on line 8

简介
----

<span class="ooclass">**Error**</span> 是所有PHP内部错误类的基类。

类摘要
------

**Error**

<span class="ooclass"> class **Error** </span> <span class="ooclass">
<span class="modifier">implements</span> **Throwable** </span> {

/\* 属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 方法 \*/

<span class="modifier">public</span> <span
class="methodname">\_\_construct</span> (\[ <span
class="methodparam"><span class="type">string</span> `$message`<span
class="initializer"> = ""</span></span> \[, <span
class="methodparam"><span class="type">int</span> `$code`<span
class="initializer"> = 0</span></span> \[, <span
class="methodparam"><span class="type">Throwable</span> `$previous`<span
class="initializer"> = **`null`**</span></span> \]\]\] )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span class="methodname">getCode</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span class="methodname">getFile</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span class="methodname">getLine</span> (
<span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span class="methodname">getTrace</span>
( <span class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">\_\_clone</span> ( <span
class="methodparam">void</span> )

}

属性
----

`message`  
错误消息内容

`code`  
错误代码

`file`  
抛出错误的文件名

`line`  
抛出错误的行数

简介
----

<span class="ooclass">**ArgumentCountError**</span>
当传递给用户定义的函数或方法的参数太少时被抛出。

类摘要
------

**ArgumentCountError**

<span class="ooclass"> class **ArgumentCountError** </span> <span
class="ooclass"> <span class="modifier">extends</span> **TypeError**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Error::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

<span class="ooclass">**ArithmeticError**</span>
当执行数学运算时发生错误时被抛出。PHP 7.0 these errors include
attempting to perform a bitshift by a negative amount, and any call to
<span class="function">intdiv</span> that would result in a value
outside the possible bounds of an <span class="type">integer</span>.

类摘要
------

**ArithmeticError**

<span class="ooclass"> class **ArithmeticError** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Error** </span>
{

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Error::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

<span class="ooclass">**AssertionError**</span> 在函数 <span
class="function">assert</span> 断言失败时被抛出。

类摘要
------

**AssertionError**

<span class="ooclass"> class **AssertionError** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Error** </span>
{

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Error::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

<span class="ooclass">**DivisionByZeroError**</span>
当除数为零时被抛出。

类摘要
------

**DivisionByZeroError**

<span class="ooclass"> class **DivisionByZeroError** </span> <span
class="ooclass"> <span class="modifier">extends</span>
**ArithmeticError** </span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Error::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

<span class="ooclass">**CompileError**</span>
是针对一些编译错误抛出的，之前是会发出致命错误。

类摘要
------

**CompileError**

<span class="ooclass"> class **CompileError** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Error** </span>
{

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Error::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

<span class="ooclass">**ParseError**</span> 当解析 PHP
代码时发生错误时抛出，比如当 <span
class="function">eval</span>被调用出错时。

> **Note**: <span class="simpara"> 从 PHP 7.3.0 开始，<span
> class="classname">ParseError</span> 继承自 <span
> class="classname">CompileError</span>。之前的版本，则继承自 <span
> class="classname">Error</span>。 </span>

类摘要
------

**ParseError**

<span class="ooclass"> class **ParseError** </span> <span
class="ooclass"> <span class="modifier">extends</span> **CompileError**
</span> {

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Error::\_\_clone</span> ( <span
class="methodparam">void</span> )

}

简介
----

有三种情况会抛出 <span
class="ooclass">**TypeError**</span>。第一种，传递给函数的参数类型与函数预期声明的参数类型不匹配；第二种，函数返回的值与声明的函数返回类型不匹配；第三种，调用
PHP 内置函数时，传递了非法的数字参数（仅限在严格模式下 / strict mode）。

类摘要
------

**TypeError**

<span class="ooclass"> class **TypeError** </span> <span
class="ooclass"> <span class="modifier">extends</span> **Error** </span>
{

/\* 继承的属性 \*/

<span class="modifier">protected</span> <span class="type">string</span>
`$message` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$code` ;

<span class="modifier">protected</span> <span class="type">string</span>
`$file` ;

<span class="modifier">protected</span> <span class="type">int</span>
`$line` ;

/\* 继承的方法 \*/

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getMessage</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">Throwable</span> <span
class="methodname">Error::getPrevious</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">mixed</span> <span
class="methodname">Error::getCode</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getFile</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">int</span> <span
class="methodname">Error::getLine</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">array</span> <span
class="methodname">Error::getTrace</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span class="modifier">public</span>
<span class="type">string</span> <span
class="methodname">Error::getTraceAsString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">public</span> <span class="type">string</span>
<span class="methodname">Error::\_\_toString</span> ( <span
class="methodparam">void</span> )

<span class="modifier">final</span> <span
class="modifier">private</span> <span class="type">void</span> <span
class="methodname">Error::\_\_clone</span> ( <span
class="methodparam">void</span> )

}
