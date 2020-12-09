Serializable::serialize
=======================

对象的字符串表示

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">string</span> <span
class="methodname">Serializable::serialize</span> ( <span
class="methodparam">void</span> )

返回对象的字符串表示。

### 参数

此函数没有参数。

### 返回值

返回对象的字符串表示或者 **`null`** 。

### 错误／异常

如果返回除了字符串或 **`null`** 之外的其他类型，将抛出 <span
class="classname">Exception</span>。

### 参见

-   <a href="/language/oop5/magic.html#object.sleep" class="link">__sleep()</a>
-   <a href="/language/oop5/magic.html#object.serialize" class="link">__serialize()</a>
