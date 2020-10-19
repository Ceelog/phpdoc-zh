Serializable::unserialize
=========================

构造对象

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">Serializable::unserialize</span> ( <span
class="methodparam"><span class="type">string</span>
`$serialized`</span> )

在反序列化对象时被调用。

> **Note**:
>
> 这个方法担当着对象<a href="/language/oop5/decon.html#language.oop5.decon.constructor" class="link">构造器</a>的角色。在此方法之后，<a href="/language/oop5/decon.html#object.construct" class="link">__construct()</a>
> 将*不会*被调用。

### 参数

`serialized`  
对象的字符串表示

### 返回值

返回没有序列化之前的原始值。

### 参见

-   <a href="/language/oop5/magic.html#object.wakeup" class="link">__wakeup()</a>
-   <a href="/language/oop5/magic.html#object.unserialize" class="link">__unserialize()</a>
