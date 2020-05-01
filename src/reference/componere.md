Componere\\cast
===============

Casting

### 说明

<span class="type">Type</span> <span
class="methodname">Componere\\cast</span> ( <span
class="methodparam"><span class="type">Type</span> `$type`</span> ,
<span class="methodparam"> `$object`</span> )

### 参数

`type`  
A user defined type

`object`  
An object with a user defined type compatible with <span
class="exceptionname">Type</span>

### 返回值

An <span class="type">object</span> of type <span
class="exceptionname">Type</span>, cast from `object`

### Exceptions

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if the
type of `object` is or is derived from an internal class

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if <span
class="exceptionname">Type</span> is an interface

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if <span
class="exceptionname">Type</span> is a trait

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if <span
class="exceptionname">Type</span> is an abstract

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if <span
class="exceptionname">Type</span> is not compatible with the type of
`object`

### 参见

-   <a href="/reference/componere.html#Componere\cast_by_ref" class="xref"></a>

Componere\\cast\_by\_ref
========================

Casting

### 说明

<span class="type">Type</span> <span
class="methodname">Componere\\cast\_by\_ref</span> ( <span
class="methodparam"><span class="type">Type</span> `$type`</span> ,
<span class="methodparam"> `$object`</span> )

### 参数

<span class="exceptionname">type</span>  
A user defined type

`object`  
An object with a user defined type compatible with <span
class="exceptionname">Type</span>

### 返回值

An <span class="type">object</span> of type <span
class="exceptionname">Type</span>, cast from `object`, where members are
references to `object` members

### Exceptions

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if the
type of `object` is or is derived from an internal class

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if <span
class="exceptionname">Type</span> is an interface

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if <span
class="exceptionname">Type</span> is a trait

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if <span
class="exceptionname">Type</span> is an abstract

**Warning**

Shall throw <span class="type">InvalidArgumentException</span> if <span
class="exceptionname">Type</span> is not compatible with the type of
`object`

### 参见

-   <a href="/reference/componere.html#Componere\cast" class="xref"></a>

**目录**

-   [Componere\\cast](/reference/componere.html#Componere\cast) —
    Casting
-   [Componere\\cast\_by\_ref](/reference/componere.html#Componere\cast_by_ref)
    — Casting
