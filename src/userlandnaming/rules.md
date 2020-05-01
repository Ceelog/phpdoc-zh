规则
----

以下列表指出了 PHP
工程在选择新的内部标识符时保留给自己的权利。最终指南是官方的<a href="https://git.php.net/?p=php-src.git;a=blob_plain;f=CODING_STANDARDS.md;hb=HEAD" class="link external">» 编码标准</a>：

-   PHP
    拥有最顶层命名空间，但是会尝试找到合体的描述命名以避免任何明显的冲突。

-   函数名在两个词中间使用下划线，类名则同时使用 *camelCase* 和
    *PascalCase* 规则。

-   PHP
    在任何扩展库的全局符号前附加上扩展库的名称（此规则在过去则有无数例外）。例如：

    -   <span class="function">curl\_close</span>

    -   <span class="function">mysql\_query</span>

    -   PREG\_SPLIT\_DELIM\_CAPTURE

    -   new DOMDocument()

    -   <span class="function">strpos</span>（以前的一个失误例子）

    -   new SplFileObject()

-   Iterators 和 Exceptions 则只是简单加上 "*Iterator*" 和 "*Exception*"
    后缀。例如：

    -   <span class="classname">ArrayIterator</span>

    -   <span class="classname">LogicException</span>

-   PHP 保留所有以 *\_\_* 开头的符号作为魔术符号。建议用户不要在 PHP
    中创建以 *\_\_*
    打头的符号，除非是要使用有文档记载的魔术函数功能。例如：

    -   <a href="/language/oop5/overloading.html#object.get" class="link">__get()</a>

    -   <span class="function">\_\_autoload</span>
