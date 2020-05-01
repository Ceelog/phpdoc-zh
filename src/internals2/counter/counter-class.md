简介
----

表示一个独立的计数器对象。

类摘要
------

**Counter**

<span class="ooclass"> class **Counter**</span> {

<span class="methodname">\_\_construct</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> \[,
<span class="methodparam"><span class="type">integer</span>
`$initial_value`</span> \[, <span class="methodparam"><span
class="type">integer</span> `$flags`</span> \]\] )

<span class="type">integer</span> <span
class="methodname">getValue</span> ( <span
class="methodparam">void</span> )

<span class="type">void</span> <span class="methodname">bumpValue</span>
( <span class="methodparam"><span class="type">integer</span>
`$offset`</span> )

<span class="type">void</span> <span
class="methodname">resetValue</span> ( <span
class="methodparam">void</span> )

<span class="type">mixed</span> <span class="methodname">getMeta</span>
( <span class="methodparam"><span class="type">integer</span>
`$attribute`</span> )

<span class="modifier">static</span> <span class="type">Counter</span>
<span class="methodname">getNamed</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

<span class="modifier">static</span> <span class="type">void</span>
<span class="methodname">setCounterClass</span> ( <span
class="methodparam"><span class="type">string</span> `$name`</span> )

}

**目录**

-   [Counter::\_\_construct](/internals2/counter/counter-class/construct.html)
    — 创建一个包含单一数值的计数器实例。
-   [Counter::getValue](/internals2/counter/counter-class/getValue.html)
    — 获取计数器的当前值。
-   [Counter::bumpValue](/internals2/counter/counter-class/bumpValue.html)
    — 修改计数器的当前值。
-   [Counter::resetValue](/internals2/counter/counter-class/resetValue.html)
    — 重置计数器的当前值。
-   [Counter::getMeta](/internals2/counter/counter-class/getMeta.html) —
    返回计数器的部分元信息。
-   [Counter::getNamed](/internals2/counter/counter-class/getNamed.html)
    — 取回一个名称已存在的计数器。
-   [Counter::setCounterClass](/internals2/counter/counter-class/setCounterClass.html)
    — 设置由 Counter::getNamed 返回的计数器类。
