ArrayAccess::offsetSet
======================

设置一个偏移位置的值

### 说明

<span class="modifier">abstract</span> <span
class="modifier">public</span> <span class="type">void</span> <span
class="methodname">ArrayAccess::offsetSet</span> ( <span
class="methodparam"><span class="type">mixed</span> `$offset`</span> ,
<span class="methodparam"><span class="type">mixed</span>
`$value`</span> )

为指定的偏移位置设置一个值。

### 参数

`offset`  
待设置的偏移位置。

`value`  
需要设置的值。

### 返回值

没有返回值。

### 注释

> **Note**:
>
> 如果另一个值不可用，那么 `offset` 参数将被设置为
> **`null`**，就像下面的例子。
>
> ``` php
> <?php
> $arrayaccess[] = "first value";
> $arrayaccess[] = "second value";
> print_r($arrayaccess);
> ?>
> ```
>
> 以上例程会输出：
>
>     Array
>     (
>         [0] => first value
>         [1] => second value
>     )
