预定义类
--------

本节列出标准的预定义类。各种扩展库定义了其它类，其说明在各自的参考文档中。

### 标准类

这些类由一些内建在 PHP 中的标准函数定义。

<span class="classname">Directory</span>  
<span class="simpara"> 由<span class="function">dir</span>创建. </span>

<span class="classname">stdClass</span>  
<span class="simpara"> Created by
<a href="/language/types/object.html#language.types.object.casting" class="link">typecasting to object</a>.
</span>

<span class="classname">\_\_PHP\_Incomplete\_Class</span>  
<span class="simpara"> Possibly created by <span
class="function">unserialize</span>. </span>

### 自 PHP 5 起预定义的类

这些额外的预定义类是 PHP 5.0.0 引进的。

<span class="classname">exception</span>  
<span class="simpara"> </span>

<span class="classname">ErrorException</span>  
<span class="simpara"> Available since PHP 5.1.0. </span>

<span class="classname">php\_user\_filter</span>  
<span class="simpara"> </span>

### Closure

PHP5.3.0中引入了一个预定义的final类<span
class="classname">Closure</span>，它可以用于实现
<a href="/functions/anonymous.html" class="link">匿名函数</a>

关于更多信息，可以查看<a href="/class/closure.html" class="link">匿名函数</a>.

### Generator

The predefined final class <span class="classname">Generator</span> was
introduced in PHP 5.5.0. It is used for representing
<a href="/language/generators.html" class="link">generators</a>.

For more information, see its
<a href="/class/generator.html" class="link">class page</a>.

### 从PHP 7开始预定义的类和接口

这些预定义的类和接口是在PHP 7.0.0 中开始引入的。

<span class="classname">ArithmeticError</span>  
<span class="simpara"> </span>

<span class="classname">AssertionError</span>  
<span class="simpara"> </span>

<span class="classname">DivisionByZeroError</span>  
<span class="simpara"> </span>

<span class="classname">Error</span>  
<span class="simpara"> </span>

<span class="classname">Throwable</span>  
<span class="simpara"> </span>

<span class="classname">ParseError</span>  
<span class="simpara"> </span>

<span class="classname">TypeError</span>  
<span class="simpara"> </span>

### 特殊的类

以下这些标识符由于它们有特殊的用处，因此不可作为类名

<span class="classname">self</span>  
<span class="simpara">
<a href="/language/oop5/paamayim-nekudotayim.html" class="link">Current class</a>.
</span>

<span class="classname">static</span>  
<span class="simpara">
<a href="/language/oop5/late-static-bindings.html" class="link">Current class in runtime</a>.
</span>

<span class="classname">parent</span>  
<span class="simpara">
<a href="/language/oop5/paamayim-nekudotayim.html" class="link">Parent class</a>.
</span>
