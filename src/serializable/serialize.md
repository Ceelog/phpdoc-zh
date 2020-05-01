Serializable::serialize
=======================

对象的字符串表示

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">Serializable::serialize</span> ( <span
class="methodparam">void</span> )

返回对象的字符串表示。

> **Note**:
>
> 这个方法担当着对象<a href="/language/oop5/decon.html#language.oop5.decon.destructor" class="link">析构器</a>的角色。在此方法之后，<a href="/language/oop5/decon.html#object.destruct" class="link">__destruct()</a>
> 方法将*不会*被调用。

### 参数

此函数没有参数。

### 返回值

返回对象的字符串表示或者 **`NULL`** 。

### 错误／异常

如果返回除了字符串或 **`NULL`** 之外的其他类型，将抛出 <span
class="classname">Exception</span>。

### 参见

-   <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
