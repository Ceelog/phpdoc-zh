PHP 7 错误处理
--------------

PHP 7 改变了大多数错误的报告方式。不同于传统（PHP
5）的错误报告机制，现在大多数错误被作为 <span
class="classname">Error</span> 异常抛出。

这种 <span class="classname">Error</span> 异常可以像 <span
class="classname">Exception</span> 异常一样被第一个匹配的 *try* /
*catch* 块所捕获。如果没有匹配的
<a href="/language/exceptions.html#language.exceptions.catch" class="link"><em>catch</em></a>
块，则调用异常处理函数（事先通过 <span
class="function">set\_exception\_handler</span> 注册）进行处理。
如果尚未注册异常处理函数，则按照传统方式处理：被报告为一个致命错误（Fatal
Error）。

<span class="classname">Error</span> 类并非继承自 <span
class="classname">Exception</span> 类，所以不能用
`catch (Exception $e) { ... }` 来捕获 <span
class="classname">Error</span>。你可以用
`catch (Error $e) { ... }`，或者通过注册异常处理函数（ <span
class="function">set\_exception\_handler</span>）来捕获 <span
class="classname">Error</span>。

### <span class="classname">Error</span> 层次结构

-   <span class="simpara"><span
    class="classname">Throwable</span></span>
    -   <span class="simpara"><span
        class="classname">Error</span></span>
        -   <span class="simpara"><span
            class="classname">ArithmeticError</span></span>
            -   <span class="simpara"><span
                class="classname">DivisionByZeroError</span></span>
        -   <span class="simpara"><span
            class="classname">AssertionError</span></span>
        -   <span class="simpara"><span
            class="classname">CompileError</span></span>
            -   <span class="simpara"><span
                class="classname">ParseError</span></span>
        -   <span class="simpara"><span
            class="classname">TypeError</span></span>
            -   <span class="simpara"><span
                class="classname">ArgumentCountError</span></span>
    -   <span class="simpara"><span
        class="classname">Exception</span></span>
        -   <span class="simpara">...</span>
