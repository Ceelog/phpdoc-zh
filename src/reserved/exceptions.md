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
class="initializer"> = **`NULL`**</span></span> \]\]\] )

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
class="initializer"> = **`NULL`**</span></span> \]\]\]\]\]\] )

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
