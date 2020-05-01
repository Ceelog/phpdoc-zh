ArrayAccess::offsetGet
======================

获取一个偏移位置的值

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">mixed</span> <span
class="methodname">ArrayAccess::offsetGet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> )

返回指定偏移位置的值。

当检查一个偏移位置是否为 <span class="function">empty</span>
时，此方法被执行。

### 参数

`offset`  
需要获取的偏移位置。

### 注释

> **Note**:
>
> Starting with PHP 5.3.4, the prototype checks were relaxed and it's
> possible for implementations of this method to return by reference.
> This makes indirect modifications to the overloaded array dimensions
> of <span class="classname">ArrayAccess</span> objects possible.
>
> A direct modification is one that replaces completely the value of the
> array dimension, as in *$obj\[6\] = 7*. An indirect modification, on
> the other hand, only changes part of the dimension, or attempts to
> assign the dimension by reference to another variable, as in
> *$obj\[6\]\[7\] = 7* or *$var =& $obj\[6\]*. Increments with *++* and
> decrements with *--* are also implemented in a way that requires
> indirect modification.
>
> While direct modification triggers a call to <span
> class="function">ArrayAccess::offsetSet</span>, indirect modification
> triggers a call to <span
> class="function">ArrayAccess::offsetGet</span>. In that case, the
> implementation of <span class="function">ArrayAccess::offsetGet</span>
> must be able to return by reference, otherwise an **`E_NOTICE`**
> message is raised.

### 返回值

可返回任何类型。

### 参见

-   <span class="methodname">ArrayAccess::offsetExists</span>
