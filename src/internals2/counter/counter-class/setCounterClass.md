Counter::setCounterClass
========================

设置由 <span class="methodname">Counter::getNamed</span>
返回的计数器类。

### 说明

<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">Counter::setCounterClass</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="function">Counter::setCounterClass</span> 改变由 <span
class="function">Counter::getNamed</span>
返回的对象的类。要设置的类可以没有 pulic 的构造器，但必须是 <span
class="classname">Counter</span>
的子类。如果不满足这些条件，则会引发致命错误。这是静态函数。

### 参数

`name`  
<span class="simpara"> 要使用的类名。 </span>
